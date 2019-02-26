function myFunction() {
  //メッセージボックスを出す
  var result = Browser.msgBox("こんにちは", Browser.Buttons.OK_CANCEL);
  if (result == "cancel"){
    Logger.log("canceled...")
  }
  
  //メッセージボックスで選択肢を出す
  var result = Browser.msgBox("選んで", "あなたはクロームユーザー？", Browser.Buttons.OK_CANCEL);
  if(result == "yes"){
    Browser.msgBox("やった")
  } else {
    Browser.msgBox("残念")
  }
  
  //入力するメッセージボックス
  var result = Browser.inputBox("御名前は？", "御名前をどうぞ:", Browser.Buttons.OK_CANCEL);
  if (result != "cancel"){
    Browser.msgBox("こんにちは" + result + "さん");
  }
