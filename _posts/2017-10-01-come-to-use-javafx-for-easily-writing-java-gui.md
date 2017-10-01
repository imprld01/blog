---
layout		: post
title		: "快來使用JavaFX輕鬆撰寫Java GUI"
subtitle	: "Come to use JavaFX for easily writing Java GUI"
date		: 2017-10-01 22:37:00 +0800
categories	: tech-note
author		: "BW"
tags		: Tech-Note Java GUI JavaFX
comments	: true
signature	: false
keywords	: Java,tutorial,教學,包裝,程式碼,java程式碼,gui,GUI,Java GUI,Eclipse,fxml,e(fx)clipse,Scene Builder,WindowBuilder,java Swing,java AWT,AWT/Swing,UI,Graphical User Interface,Java視窗程式,視窗程式
description	: 電腦的普及起源於電腦的方便使用。現在使用電腦十分容易，只要按一下開機鍵就可以開始登入電腦，想要打開任何軟體只要點擊兩下就可以，回顧過去，曾經的電腦可是要輸入指令才能運作的，有使用過PTT的讀者應該就能體會現今電腦的圖形化介面實在是十分友善。而寫程式不是只要將問題解答出來就好，一個完美的資訊工作者應該要能兼顧解決問題的程式能力以及運用方法將結果呈現出來的能力，像是你可以撰寫一個APP呈現結果，或者撰寫一個網站，亦或是撰寫一個視窗程式，這些方式皆是十分有效的表現方式，比起呈現複雜的文字或者程式碼，人們對於圖形的接受度還是比較高。目前許多語言都有一些套件可以撰寫圖形化介面，而圖形化介面實際上也是一門學問，其中牽扯到使用者介面(User Interface, UI)以及使用者經驗(User Experience, UX)。
---

[<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/JavaFX_Logo.png" alt="Python"></span>](https://en.wikipedia.org/wiki/File:JavaFX_Logo.png)
電腦的普及起源於電腦的方便使用。現在使用電腦十分容易，只要按一下開機鍵就可以開始登入電腦，想要打開任何軟體只要點擊兩下就可以，回顧過去，曾經的電腦可是要輸入指令才能運作的，有使用過PTT的讀者應該就能體會現今電腦的圖形化介面實在是十分友善。而寫程式不是只要將問題解答出來就好，一個完美的資訊工作者應該要能兼顧解決問題的程式能力以及運用方法將結果呈現出來的能力，像是你可以撰寫一個APP呈現結果，或者撰寫一個網站，亦或是撰寫一個視窗程式，這些方式皆是十分有效的表現方式，比起呈現複雜的文字或者程式碼，人們對於圖形的接受度還是比較高。目前許多語言都有一些套件可以撰寫圖形化介面，而圖形化介面實際上也是一門學問，其中牽扯到使用者介面(User Interface, UI)以及使用者經驗(User Experience, UX)。

<blockquote class="bq_setting">
圖形化(Graphical)：
(1) 使用者介面(User Interface)：使用者接觸產品的部分，例如外觀(設計者專注於風格呈現)
(2) 使用者經驗(User Experience)：使用者使用產品的感覺，例如互動(設計者專注於流程體驗)
</blockquote>

[<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/uiux.png" alt="UI and UX"></span>](https://careerfoundry.com/en/blog/ux-design/the-difference-between-ux-and-ui-design-a-laymans-guide/)

說到Java的視窗程式，無非就是使用Java AWT/Swing來開發視窗程式，但是令人頭痛的是Java所提供的介面圖型並不好看，而且還要直接用撰寫程式碼的方式來開發，光是要建構一個計算機的GUI就要耗上大半的開發時間，如果要微調或者更改設計，就又要花大半的時間埋首於一堆程式碼中。幸好Eclipse上有插件可以提供開發者使用拖拉的方式迅速完成GUI並產出相關的程式碼，這樣便能方便開發者將精力放在解決困難的問題上，但是千萬別放棄使用Java開發視窗程式的念頭，因為後來Oracle開發出更好使用的GUI套件－JavaFX。JavaFX其實早在2008年就出現了，只是它並未內建在Java中，後來2014年Oracle公司發佈Java 8之後，JavaFX不再作為獨立的JavaFX SDK，而是直接內建在Java Runtime Environment(JRE)與Java Development Kit(JDK)中，與傳統的AWT/Swing比較，JavaFX提供更多更好的工具與函式庫幫助開發者開發視窗程式，而且其程式效能更加快速、圖形更具現代感。

<blockquote class="bq_setting">
系統實作守則－MVC(Model-View-Controller)：
(1) 邏輯的部分(Model)：系統中處理的核心
(2) 顯示的部分(View)：系統中的使用者介面
(3) 協調的部分(Controller)：系統中負責轉介資料與處理核心
</blockquote>

本篇的重點不在如何設計UI或UX，而是將重點放在設計階段之後的實作，所以後續將會介紹使用Java建構一個視窗程式的基本概念。不過在實際介紹之前，小編希望帶給各位系統實作的原則－MVC(Model-View-Controller)模式，這是軟體工程(Software Engineering)中目前十分受歡迎並被廣泛接受的架構。其中的Model注重於處理系統中解決問題的邏輯與演算法；View則注重於呈現系統中的使用者介面並接收使用者的資訊；而Controller則是負責協調介於兩者之間的工作分配。舉例來說，使用者在網頁的表單(View)上輸入帳號與密碼(Data)，依照網頁表單指定的方式將使用者輸入的帳號與密碼(Data)傳送至後台的程式(Controller)處理，後台的程式(Controller)為了完成審核帳號與密碼的工作會呼叫其他程式(Model)來幫忙，例如呼叫資料庫連結的程式碼、查詢帳號與密碼的程式碼、審核帳號與密碼的程式碼等，最後由這些多個其他程式(Models)完成工作後，再由後台的程式(Controller)將結果傳回至網頁(View)上呈現。MVC的概念就好比是現實職場上，客戶、經理與員工的角色與職責分配。MVC的重點在於將系統中不同層面的工作區分開來，目的在於建構具有系統性的系統架構，好處在於方便後續的維護與管理，乃至於新相關程式碼的變更，當然這樣的原則也能幫助開發者開發時能有清晰的架構與思維撰寫相對應的程式碼，在團隊的分工合作上也是具有相當大的助益。

[<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/MVC.jpg" alt="MVC"></span>](http://140.138.149.49/N22/final_report/web/AM/)

首先我們先來回顧一下過去要如何使用Eclipse加速開Java AWT/Swing吧。

* ⚫️ 在Eclipse上開發Java AWT/Swing：環境安裝

<blockquote class="bq_setting">
環境準備：<br/>
(1) <a style="color:black;" target="_blank" href="http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html">Java Runtime Environment(JRE)</a><br>
(2) <a style="color:black;" target="_blank" href="http://www.eclipse.org/downloads/eclipse-packages/">Eclipse IDE for Java</a><br>
(3) <a style="color:black;" target="_blank" href="http://www.eclipse.org/windowbuilder/download.php">WindowBuilder</a>
</blockquote>

<div class="sp_setting">步驟1</div>
安裝Eclipse之前需要先行安裝JRE，讀者可以參考<a style="color:black;" target="_blank" href="https://imprld01.github.io/blog/tech-note/2017/10/01/java-runtime-environment-8-installation/">此篇</a>。

<div class="sp_setting">步驟2</div>
接著安裝Eclipse，安裝Eclipse的流程讀者可以參考<a style="color:black;" target="_blank" href="https://imprld01.github.io/blog/tech-note/2017/10/01/eclipse-ide-installation/">此篇</a>。

<div class="sp_setting">步驟3</div>
至<a style="color:black;" target="_blank" href="http://www.eclipse.org/windowbuilder/download.php">WindowBuilder</a>的官方網站上，選擇符合版本的Eclipse，並在其下載連結上點擊右鍵，事先複製下載網址，該網址會在後續步驟中用到。例如，小編的Eclipse版本為4.7，所以小編便複製該列Release Version的link，由於該連結不存在，所以小編就複製了Integration Version的link。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/1-1.JPG"></span>

<div class="sp_setting">步驟4</div>
開啟Eclipse IDE，點選Help>Install New Software。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/1-2.JPG"></span>

<div class="sp_setting">步驟5</div>
點選右邊的Add。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/1-3.JPG"></span>

<div class="sp_setting">步驟6</div>
在Name欄位上填寫WindowBuilder，在Location欄位貼上步驟3複製下來的網址，然後按下OK。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/1-4.JPG"></span>

<div class="sp_setting">步驟7</div>
將中間列出的所有套件勾選後按下Next。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/1-5.JPG"></span>

<div class="sp_setting">步驟8</div>
確認所有即將安中的套件後按下Next。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/1-6.JPG"></span>

<div class="sp_setting">步驟9</div>
選擇接受同意書內容後按下Finish。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/1-7.JPG"></span>

<div class="sp_setting">步驟11</div>
等待安裝程序完成，最後點選Yes重新啟動Eclipse，WindowBuilder便安裝完成。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/1-8.JPG"></span>

* ⚫️ 在Eclipse上開發Java AWT/Swing：初次使用

<blockquote class="bq_setting">
環境要求：
(1) <a style="color:black;" target="_blank" href="http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html">Java Runtime Environment(JRE)</a><br>
(2) <a style="color:black;" target="_blank" href="http://www.eclipse.org/downloads/eclipse-packages/">Eclipse IDE for Java</a><br>
(3) <a style="color:black;" target="_blank" href="http://www.eclipse.org/windowbuilder/download.php">WindowBuilder</a>
</blockquote>

<div class="sp_setting">步驟1</div>
開啟Eclipse。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/2-1.JPG"></span>

<div class="sp_setting">步驟2</div>
新增一個新的Java專案。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/2-2.JPG"></span>

<div class="sp_setting">步驟3</div>
為專案命名，小編命名的習慣是每個單詞首字大寫並使用減號隔開。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/2-3.JPG"></span>

<div class="sp_setting">步驟4</div>
在專案中點擊右鍵，選擇New>Other。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/2-4.JPG"></span>

<div class="sp_setting">步驟5</div>
在專案中新增WindowBuilder>Swing Designer>Application Window。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/2-5.JPG"></span>

<div class="sp_setting">步驟6</div>
為應用程式命名，小編命名的習慣是每個單詞首字大寫並不用任何字元隔開。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/2-6.JPG"></span>

<div class="sp_setting">步驟7</div>
可以見到基礎的程式碼已經產生。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/2-7.JPG"></span>

<div class="sp_setting">步驟8</div>
轉換至Design模式後，可以見到對應的圖形化結果。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/2-8.JPG"></span>

<div class="sp_setting">步驟9</div>
接下來開發者可以依照需求進行拖曳與配置。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/2-9.JPG"></span>

<div class="sp_setting">步驟10</div>
拖曳之後，轉換回Source模式，可以發現對應的程式碼也被產生出來。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/2-10.JPG"></span>

* ⚫️ 在NetBeans上開始使用JavaFX：環境安裝

<blockquote class="bq_setting">
環境準備：
(1) <a style="color:black;" target="_blank" href="http://www.oracle.com/technetwork/java/javase/downloads/index.html">NetBeans IDE</a><br>
(2) <a style="color:black;" target="_blank" href="http://www.oracle.com/technetwork/java/javase/downloads/javafxscenebuilder-info-2157684.html">JavaFX Scene Builder 2.0</a>
</blockquote>

<div class="sp_setting">步驟1</div>
首先安裝NetBeans，安裝NetBeans的流程讀者可以參考<a style="color:black;" target="_blank" href="https://imprld01.github.io/blog/tech-note/2017/10/01/netbeans-ide-installation/">此篇</a>。

<div class="sp_setting">步驟2</div>
接著至官方網站，選擇下載與系統環境相符的安裝執行檔，小編的環境是Windows x64，所以選擇javafx-scenebuilder-2_0-windows.msi。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/3-1.JPG"></span>

<div class="sp_setting">步驟3</div>
找到電腦中下載完成的安裝執行檔，雙點擊該安裝執行檔。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/3-2.JPG"></span>

<div class="sp_setting">步驟4</div>
點擊下一步開始設定安裝配置。。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/3-3.JPG"></span>

<div class="sp_setting">步驟5</div>
選擇並確認JavaFX Scene Builder的安裝路徑(預設路徑即可)後，點選安裝來啟動安裝程式。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/3-4.JPG"></span>

<div class="sp_setting">步驟6</div>
等待安裝完成後，最後按下完成結束安裝，JavaFX Scene Builder便安裝完成。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/3-5.JPG"></span>

* ⚫️ 在NetBeans上開始使用JavaFX：初次使用
 
<blockquote class="bq_setting">
環境準備：
(1) <a style="color:black;" target="_blank" href="http://www.oracle.com/technetwork/java/javase/downloads/index.html">NetBeans IDE</a><br>
(2) <a style="color:black;" target="_blank" href="http://www.oracle.com/technetwork/java/javase/downloads/javafxscenebuilder-info-2157684.html">JavaFX Scene Builder 2.0</a>
</blockquote>

<div class="sp_setting">步驟1</div>
開啟NetBeans。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/4-1.JPG"></span>

<div class="sp_setting">步驟2</div>
新增專案。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/4-2.JPG"></span>

<div class="sp_setting">步驟3</div>
選擇新增JavaFX FXML Application。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/4-3.JPG"></span>

<div class="sp_setting">步驟3</div>
為應用程式命名，同時這也會式專案的名稱，小編命名的習慣是每個單詞首字大寫並不用任何字元隔開。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/4-4.JPG"></span>

<div class="sp_setting">步驟4</div>
可以見到基礎的程式碼已經產生。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/4-5.JPG"></span>

<div class="sp_setting">步驟5</div>
雙點擊FXML檔案便可以透過JavaFX Scene Builder開啟應用程式的圖形化介面，開發者可以隨需求進行拖曳與版面配置。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/4-6.JPG"></span>

* ⚫️ 在Eclipse上開始使用JavaFX：環境安裝

<blockquote class="bq_setting">
環境準備：
(1) <a style="color:black;" target="_blank" href="http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html">Java Runtime Environment(JRE)</a><br>
(2) <a style="color:black;" target="_blank" href="http://www.eclipse.org/downloads/eclipse-packages/">Eclipse IDE for Java</a><br>
(3) <a style="color:black;" target="_blank" href="http://www.eclipse.org/efxclipse/install.html">e(fx)clipse</a><br>
(4) <a style="color:black;" target="_blank" href="http://www.oracle.com/technetwork/java/javase/downloads/javafxscenebuilder-info-2157684.html">JavaFX Scene Builder 2.0</a>
</blockquote>

<div class="sp_setting">步驟1</div>
安裝Eclipse之前需要先行安裝JRE，讀者可以參考<a style="color:black;" target="_blank" href="https://imprld01.github.io/blog/tech-note/2017/10/01/java-runtime-environment-8-installation/">此篇</a>。

<div class="sp_setting">步驟2</div>
接著安裝Eclipse，安裝Eclipse的流程讀者可以參考<a style="color:black;" target="_blank" href="https://imprld01.github.io/blog/tech-note/2017/10/01/eclipse-ide-installation/">此篇</a>。

<div class="sp_setting">步驟3</div>
複製此段網址：http://download.eclipse.org/efxclipse/updates-released/2.4.0/site，該網址會在後續步驟中用到，其版本可於e(fx)clipse官方網站查得。

<div class="sp_setting">步驟4</div>
開啟Eclipse IDE，點選Help>Install New Software。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/5-1.JPG"></span>

<div class="sp_setting">步驟5</div>
點選右邊的Add。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/5-2.JPG"></span>

<div class="sp_setting">步驟6</div>
在Name欄位上填寫e(fx)clispe，在Location欄位貼上第3步驟複製下來的網址，最後按下OK。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/5-3.JPG"></span>

<div class="sp_setting">步驟7</div>
將中間列出的所有套件勾選後按下Next。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/5-4.JPG"></span>

<div class="sp_setting">步驟8</div>
確認所有即將安中的套件後按下Next。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/5-5.JPG"></span>

<div class="sp_setting">步驟9</div>
選擇接受同意書內容後按下Finish。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/5-6.JPG"></span>

<div class="sp_setting">步驟10</div>
等待安裝程序完成。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/5-7.JPG"></span>

<div class="sp_setting">步驟11</div>
安裝完成後，點選Yes重新啟動Eclipse。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/5-8.JPG"></span>

* ⚫️ 在Eclipse上開始使用JavaFX：初次使用
 
<blockquote class="bq_setting">
環境要求：
(1) <a style="color:black;" target="_blank" href="http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html">Java Runtime Environment(JRE)</a><br>
(2) <a style="color:black;" target="_blank" href="http://www.eclipse.org/downloads/eclipse-packages/">Eclipse IDE for Java</a><br>
(3) <a style="color:black;" target="_blank" href="http://www.eclipse.org/efxclipse/install.html">e(fx)clipse</a><br>
(4) <a style="color:black;" target="_blank" href="http://www.oracle.com/technetwork/java/javase/downloads/javafxscenebuilder-info-2157684.html">JavaFX Scene Builder 2.0</a>
</blockquote>

<div class="sp_setting">步驟1</div>
開啟Eclipse IDE。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-1.JPG"></span>

<div class="sp_setting">步驟2</div>
新增一個新的Java專案。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-2.JPG"></span>

<div class="sp_setting">步驟3</div>
為專案命名，小編命名的習慣是每個單詞首字大寫並使用減號隔開。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-3.JPG"></span>

<div class="sp_setting">步驟4</div>
在專案中點擊右鍵，選擇New>Other。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-4.JPG"></span>

<div class="sp_setting">步驟5</div>
選擇New FXML Document，新增應用程式的使用者介面，這個檔案在MVC模式中扮演的是View。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-5.JPG"></span>

<div class="sp_setting">步驟6</div>
為FXML檔案命名，小編命名的習慣是每個單詞首字大寫並不用任何字元隔開。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-6.JPG"></span>

<div class="sp_setting">步驟7</div>
在專案中點擊右鍵，選擇New>Other，並選擇JavaFX Main Class，新增應用程式的起始進入點。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-7.JPG"></span>

<div class="sp_setting">步驟8</div>
為檔案命名，小編命名的習慣是每個單詞首字大寫並不用任何字元隔開。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-8.JPG"></span>

<div class="sp_setting">步驟9</div>
在Main Class中，可以發現類別繼承Application類別，我們要做的是覆蓋父類別的start函式。我們要告訴程式起始應載入的使用者介面，並將其顯示。程式碼如下：
<script type="syntaxhighlighter" class="brush: jfx">
Parent root = FXMLLoader.load(getClass().getResource("MainPage.fxml"));
&nbsp;
Scene scene = new Scene(root);
&nbsp;
primaryStage.setScene(scene);
primaryStage.show();
</script>
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-9.JPG"></span>

<div class="sp_setting">步驟10</div>
在FXML檔案上點擊右鍵，選擇Open with SceneBuilder，可以透過JavaFX Scene Builder開啟應用程式的圖形化介面。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-10.JPG"></span>

<div class="sp_setting">步驟11</div>
開發者可以透過JavaFX Scene Builder隨需求進行拖曳與版面配置。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-11.JPG"></span>

<div class="sp_setting">步驟12</div>
小編拖曳AnchorPane為使用者介面的基底。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-12.JPG"></span>

<div class="sp_setting">步驟13</div>
接著，小編拖曳一個按鈕在使用者介面上，並將此介面存檔。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-13.JPG"></span>

<div class="sp_setting">步驟14</div>
配置完使用者介面後，我們可以看到原本的FXML檔案自動產生一些程式碼了。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-14.JPG"></span>

<div class="sp_setting">步驟15</div>
接著，我們可以再按下右鍵新增Java Class。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-15.JPG"></span>

<div class="sp_setting">步驟16</div>
為類別命名，小編命名的習慣是每個單詞首字大寫並不用任何字元隔開。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-16.JPG"></span>

<div class="sp_setting">步驟17</div>
接著，在這個類別上實作Initializable類別，這個類別扮演的是MVC模式中的Controller，開發者可以在該類別中實作事件處理函式。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-17.JPG"></span>

<div class="sp_setting">步驟18</div>
基本上的應用程式架構便建立完成，讀者可以直接運行應用程式，後續讀者可以再依需求建立需要的類別最為MVC模式中的Model。
<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171001-JavaFX/6-18.JPG"></span>