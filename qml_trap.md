MouseArea & focus
1. MouseArea will prevent tooltip showing in covered area. please consider focus if you need native tooltip for button
2. focusScope is must if you got mutilple element that take focus, vanilla component will not able to proxy focus by default

Layout:
1. don't bind the width or height that's determined by Layout. because the width/height will be adjust multiple time during layout engine.
2. same as #1, don't reply on the Component.onComplete to get the actually sizing, the sizing will change after constructed.
3. don't relay on "parent" to refer to component in containers layout class, the children may get inserted and popout with helper container, the parent may not the parent you think, so id if possible for implicit reference

Font auto fit
if fontSizeMode is dynamic adjusted to content, the font.pixelSize and font.pointSize will not be the actually font size rendered, but the default guessed value(which is pointless).