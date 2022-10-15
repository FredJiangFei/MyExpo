# Props
    style
    autoCapitalize 切换为大写
        * characters: 所有的字符。
        * words: 每个单词的第一个字符。
        * sentences: 每句话的第一个字符（默认）。
        *  none: 不切换。
    autoComplete ??????
    textAlign
        * left
        * center
        * right
    textContentType
        none
        URL
        addressCity
        addressCityAndState
        addressState
        countryName
        creditCardNumber
        emailAddress
        familyName
        fullStreetAddress
        givenName
        jobTitle
        location
        middleName
        name
        namePrefix
        nameSuffix
        nickname
        organizationName
        postalCode
        streetAddressLine1
        streetAddressLine2
        sublocality
        telephoneNumber
        username
        password
        newPassword
        oneTimeCode

    autoCorrect
        拼写自动修正
    autoFocus
        获得焦点
    blurOnSubmit ???????
        文本框在提交的时候失焦
    caretHidden
        隐藏光标
    clearButtonMode ???????
        是否要在文本框右侧显示“清除”按钮
    clearTextOnFocus
        每次开始输入的时候都会清除文本框的内容
    dataDetectorTypes ????????
        'phoneNumber'
        'link'
        'address'
        'calendarEvent'
        'none'
        'all'

    defaultValue
    editable
        文本框是否可编辑
    enablesReturnKeyAutomatically
        在文本框内没有文字的时候禁用确认按钮
# keyboardType
        所有平台都可用：
            default
            number-pad
            decimal-pad
            numeric
            email-address
            phone-pad
        iOS 可用：
            ascii-capable
            numbers-and-punctuation
            url
            name-phone-pad
            twitter
            web-search
    maxLength
    multiline
        输入多行文字
        安卓上如果设置multiline = {true}，文本默认会垂直居中，可设置textAlignVertical: 'top'样式来使其居顶显示
    numberOfLines
        设置输入框的行数。当 multiline 设置为 true 时使用它
    onFocus
        获得焦点
    onBlur
        失去焦点
    onChange
        内容变化
        回调参数为{ nativeEvent: { eventCount, target, text} }
    onChangeText
        内容变化
        改变后的文字内容会作为参数传递
    onContentSizeChange

    onEndEditing
        文本输入结束后调用此回调函数
    onKeyPress
        当一个键被按下的时候调用此回调
        { nativeEvent: { key: keyValue } }, keyValue即为被按下的键
        在 onChange 之前调用
    onLayout
        组件加载或者布局变化的时候调用
    onScroll
        内容滚动时持续调用
    onSelectionChange
        光标位置变化时调用，{ nativeEvent: { selection: { start, end } } }
    onSubmitEditing
        当软键盘的 确定/提交 按钮被按下的时候调用此函数
    onTextInput
        使用光标在某位置输入文本时调用
    placeholder
    placeholderTextColor

# returnKeyLabel(Android)
# returnKeyType(IOS/Android)
        决定“确定”按钮显示的内容
    
    secureTextEntry
        文本框会遮住之前输入的文字
    
    selection
        设置选中文字的范围
    selectionColor
    selectTextOnFocus
        如果为 true，当获得焦点的时候，所有的文字都会被选中
    
    spellCheck
        拼写检查
    
    passwordRules

# Methods
    .focus()
    .blur()
    clear()
    isFocused()
