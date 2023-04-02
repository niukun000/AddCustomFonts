# AddCustomFonts
Add fonts out of Apple library


1, Download your custom font
  I donloaded from https://www.fontsquirrel.com/
  
2, Copy font to your file
  create a seperate group folder called CustomFont and drag your font into the folder
  check copy if needed and add target to your app
  
3, Add permission to info.pilist
  open info.pilist and under custom IOS Target Properties, add a key "Fonts provided by application" 
  and add the font name you wish to the item list

4, how to use it
      lazy var label: UILabel  = {
        let label = UILabel()
        guard let custonFont = UIFont(name: "Cooper Hewitt", size: UIFont.labelFontSize) else{
            fatalError("failed to load customFont")
        }
        label.font = UIFontMetrics.default.scaledFont(for: custonFont)
        label.adjustsFontForContentSizeCategory = true
        return label
        
    }()

