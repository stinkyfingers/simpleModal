simpleModal
===========

Extremely simple Javascript modal. 


USE:
	1) Include the modal.js file in the html document:
		<script type="text/javascript" src="modal.js"></script>
	
	2) Using simple modal requires four HTML elements (e.g. divs):
		a) one or several elements that call openModal(this); html in the id attribute is what's displayed. e.g.
			<a href="#" onclick="openModal(this)" id="<p>Modal Content!</p>"> Click</a>
		b) a div that serves as the overlay (if you want a darkend background)
		c) a div that serves as the modal itself
		d) an element that calls closeModal() - cannot be inside the modal itself
	
		For example:
			<div id="callModal" onclick="openModal()">OPEN</div>
			<div id="overlay"></div>
			<div id="innerModal"></div>
			<div onclick="closeModal()" id="another">CLOSE</div>
	
	3) Set user settings (params array), by pasting this script in page or including. You can declare params in the modal.js file, in a separate file, or in the html doc
		<script type="text/javascript">
		//Simple Modal User Settings
		var params = {
			overlayID: "overlay",
			modalID: "innerModal",
			buttonID:"another",
			overlayStyleString: "background-color:black; opacity:.5; left: 0px; top: 0px; width:100%; height:100%; text-align:center; ", //keep most of these as-is
			modalStyleString: "width:50%; height:50%; margin: 10px auto; background-color: #aca; border:1px solid #000; padding:15px; text-align:center; ",
			buttonStyleString: "position: relative; top: -3em; margin: 0 auto; text-align:center; color:red"
			}
		initialParams(params);
		</script>
	
	
	4) Call initialParams() in the document, e.g.
		<body onload="initialParams();">
	