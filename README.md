# blender_textReplacementVMT
This project aims to speed up creation of VMTs for a blender model by creating them from inside blender, with the right names.
Uses a VMT "blueprint", which is basically a VMT text block with some "marker" string to be replaced.

Example:

VertexLitGeneric
{

	"$basetexture" "models/proj/[BPRINT]"  
	"$bumpmap" "models/proj/[BPRINT]"
  
	"$surfaceprop" "Bloodyflesh"

	"$phong" "1"
	"$phongfresnelranges" "[0.5 0.75 1]"
	"$phongexponent" "5"
	"$phongboost" "1.0"
}

Setting *Replacement Marker String* to [BPRINT] would make the "Replacer Entries" replace the Marker Strings in the final archive.

Entries are replaced in the order they appear in the blueprint, by the respective "Replacer Entry". Replacer Entries will loop if there are more markers than replacers.
