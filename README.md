# Low Poly Plant HDAs
 A group of low poly plant tools for Houdini. 
		-Each plant has controls for the plant shape, called "Global Plant Parameters"
		-You can also control the shape of the pot, and how the plants are duplicated
	*the tool is built for Houdini, but I included instructions for Unreal Engine below if you would like to integrate the tool directly in Unreal. 

Thank you *berry* much (dum dum tiss) for downloading this tool, feel free to use for any projects personal or commercial. Have fun~ ♥

- Amanda Nicole


If you would like to integrate this into Unreal Engine
	NOTE: they "berry" HDA requires an input of a curve, you can create this curve in Unreal Engine, however it will require a bit of work. It may be better to create this in Houdini and import it. 
		-You will have to dramatically upscale the tool to fit with Unreal Engine's scale, you can do so by 
			1. Right click, and "allow editing of contents"
			2. Go to the very end of the node network, and add a transform node to upscale the mesh
			or..
			1. Upscale each parameter individually (this is the most tedius but will produce the best results)
		-You will have to add in material slots and Layout the UVs of the mesh, you can do so by 
			1. Right click, and "allow editing of contents"
			2. Go to the "color" nodes. There should be at least 2-3 per plant.
			3. Replace the "color" nodes with either an Unreal Engine material node, or your own material node
				- you can easily see which color effects which object by clicking the yellow "bypass" icon at the top of the node, which will hide the object. 
				- you can also change the color to see what object reacts to it
			4. Use Houdini's UV toolkit or "labs auto UV" node to add UVs to the mesh. 
				-You can do this after each "color" node or before every "copy to points" mesh
					-if the copy to points contains a switch, please layout the UVs before the switch node, for optimization
		-After following these steps, you should be able to import the HDA into Unreal successfully. I have not personally tested this, so you may encounter bugs. 
		-I can release a version optimized for Unreal Engine if there is demand for it. 

