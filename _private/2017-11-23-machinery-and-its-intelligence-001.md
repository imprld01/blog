---
layout		: post
title		: "漫遊機器與智慧 001: 機器會思考了嗎?"
subtitle	: "Machinery and its Intelligence 001: Can Machines Think?"
date		: 2017-11-23 00:27:00 +0800
categories	: tech-note
author		: "BW"
tags		: Tech-Note Machine-Learning Artificial-Intelligence
comments	: true
signature	: false
keywords	: machine learning,artificial intelligence
description	: 
---

[<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171123/techOpen.jpg" alt="technology"></span>](https://pixabay.com/en/network-iot-internet-of-things-782707/)
人類會思考嗎？機器也會思考嗎？人們如何思考？機器又如何思考呢？這是一件十分有趣且神奇的問題！初次接觸這個主題的人應該跟當初的小編一樣充滿著無限的想像，從小到大看過的電影中，機器人活生生出現在人們的生活中，它(他/她)可以有意識的活動、從經驗中學習、與他人對話，就如同人類一般。

最讓我印象深刻的機器人莫過於大家童年幾乎都有接觸過的卡通－哆啦A夢，大家千萬別小看這部「兒童」卡通，這部卡通裡面充滿著我們期望的科技結晶，包括機器人－一個富有情感與能力的機器「人」。漫畫裡的機器人能夠辨認車輛、人類、建築與物品等事物，它(他/她)自由地行走在路上，能夠正確偵測危險、判斷與決策，更能夠像人類一樣吃著美味的食物、擁有感受酸甜苦辣的味蕾、媲美人類(甚至超越人類)的感官與四肢，最重要的是自然的情感流動以及與生俱來的性格。

從2016年初Alpha Go以4:1的成績打敗南韓圍棋選手－李世乭的事件開始，加上多人與新聞大力推廣，曾經想像的機器人在現代看來似乎有實現的曙光，同時也使得資訊領域變得十分熱門。但事實上，現在的機器人真的能像人類一般具有思想、意識、創作、情感、心靈、理解能力等珍貴且複雜的寶藏嗎？機器人能媲美人類的時代到來了嗎？機器人能大舉取代人類了嗎？還有，你真的有熱情在資訊領域打滾嗎？

* ⚫️ 智慧？機器？學習？思考？

要談機器人背後的科技就會談到人工智慧，尋找人工智慧相關的資料後，又會發現機器學習、資料探勘、深度學習等名詞。究竟什麼是人工智慧？什麼是機器學習？什麼是資料探勘？什麼是深度學習？這些名詞又與物聯網、雲端運算、大數據有什麼關聯？而雲端運算是什麼？物聯網是什麼？大數據又是什麼？這些名詞背後的差別是什麼？接下來就讓我們一探究竟吧。

過去是互聯網的時代，人與人、人與機器、機器與機器互相連結著，而物聯網則是互聯網的延伸，其大概念主要是如字面上所述「讓物品連上網路」，這在雲端運算與網路架構都成熟的基礎下順利發展，這裡提到的雲端運算簡單來說主要就是希望精簡客戶端的機器功能，複雜的運算則交由後端大量的伺服器「平行處理」與「分散式處理」，當然雲端運算所包含的內容不只於此，有興趣的讀者可以自行搜尋其他文章。

[<span class="image featured"><img width="512" src="{{ site.baseurl }}/assets/img/20171123/IoT.jpg" alt="internet-of-things"></span>](https://commons.wikimedia.org/wiki/File%3AInternet_of_Things.jpg)

在物聯網的興起下而誕生的名詞則是大數據，可以想像的是當世界是所有物品都具備聯網能力時，每樣物品每分每秒都在產生數據，這些數據的數量光是想像就十分可觀，這就是所謂的大數據。大數據背後隱藏著十分巨大的價值，如果我們能夠處理這些龐大的資料，將其轉變成有用的資訊，這些資訊將能創造龐大的利益。不過，如何運算這些巨量數據呢？答案是「多台高運算能力的電腦」，亦即透過大量的伺服器平行處理與分散式處理，而這也是大數據的必須的重點技術。這些數據或資訊又能夠如何被運用呢？答案是可以作為「機器人的課本」，亦即人工智慧的基礎原料。

人工智慧是個大領域，裏頭包含了許多子領域與技術，包括機器學習、資料探勘、深度學習等，當然這些技術在必要時也需要透過平行處理與分散式處理等技術加速運算。下圖總結這些名詞彼此之間的關連，而平行處理與分散式處理則是用來支持雲端運算與人工智慧的處理技術，為避免過於混亂便不置於圖中。

<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171123/techOverview.jpg" alt="tech-overview"></span>

<blockquote class="bq_setting">在雲的背後，支撐著天空的是名為盤古的電腦。</blockquote>

強大運算能力的電腦是雲端背後的支柱，電腦越加強大，輔助人類的範圍就越大，電腦如果具有智慧，這將大大改變未來的生活。而如何才能聲稱機器具有智慧？我們對於機器擁有智慧的試驗方法是依據計算機科學之父－艾倫．麥席森．圖靈(Alan Mathison Turing)在1950年提出的圖靈測試(Turing Test)：使受測者透過電傳設備與對方對話，在受測者已知對方可能為人類或機器的情況下，當受測者分辨不出對話的對象是人類還是機器時，該機器便具有智慧。

[<span class="image featured"><img width="256" src="https://upload.wikimedia.org/wikipedia/commons/3/30/Turing-test.gif" alt="turing-test"></span>](https://commons.wikimedia.org/wiki/File%3ATuring-test.gif)

但是隨後在1980年約翰．羅傑斯．希爾勒(John Rogers Searle)認為圖靈測試的結果並不能代表機器真正具有「智慧」，因此提出中文房間論證(The Chinese Room Argument)：在封閉的房間中，一個英語使用者有著一本手冊，而門外的中文使用者透過門縫向英語使用者傳遞紙條，紙條上所寫的是中文使用者對英語使用者提出的問題；英語使用者並未學會中文，但是英語使用者能根據手冊找出相對的回應，門外的中文使用者也無法得知門內的英語使用者是否懂中文。這告訴我們，機器就算能模擬出如人類般智慧的對話(智慧的外顯行為)，也不算是真正具有智慧，因為機器只是根據手冊(演算法)作出反應，並未具有任何情感與意識。

[<span class="image featured"><img width="512" src="{{ site.baseurl }}/assets/img/20171123/chineseRoom.jpg" alt="2-chinese-room"></span>](https://commons.wikimedia.org/wiki/File%3A2-chinese-room.jpg)

因此，真正的機器「人」應該是具有人類特質的機器，能如人類具有思想、意識、創作、情感、心靈、理解能力等，這些人類都不確定能完美解釋的特質，這也是目前技術最難突破的地方！那到底如何才能聲稱機器具有智慧？隨著人工智慧不斷的演進，圖靈測試的內容也不斷演進，出現許多其他版本的圖靈測試，像是「完全圖靈測試」，這部分留給有興趣的讀者研究！

「各個擊破」(Divide and Conquer)是資訊領域常常使用的概念，也是人們很常直接使用的思維方式：透過將大問題拆解成許多子問題，以此類推，進而一一解決，這便是「各個擊破」的精神。循著這樣的想法，想要創造一個真正的機器人，就可以採用這個方式。將人們腦袋中的知識拆解成許多問題，再透過研究一個問題的規則作為人工智慧的基礎，例如研究人類如何對話？人類如何創作？醫生如何藉由診斷歸納出病名？集合這些能力，機器人就能如同人類或特定職業的專家一樣。因此在1970年代左右，人們便提出專家系統(Expert System)，專門被設計來解決特定領域內由領域專家才能解決的複雜問題，其主要是透過大量的規則來代表已知的知識，以達成自動化處理的目的。不過，這樣的發展方式卻面臨更多困難的挑戰，包括問題的複雜程度、解決方法的通用性以及當時硬體上的限制。

之後人工智慧便沉寂一時，直到人們對人工智慧的態度從模擬人類對問題的思維方式轉換為模擬人類對事物的學習方式後，隨之誕生的便是機器學習、資料探勘，乃至深度學習等領域。這些領域最主要的觀念在於：透過研究統計方法，使機器閱讀資料、自行學習，甚至找出彼此之間的規則、規律或關聯性，就如同我們人類進行學習一樣。

還記得曾經在網路上看到一篇文章，裡面蒐集了現實中的科技，並與哆啦A夢的道具對照，我們可以發現哆啦A夢的道具正慢慢地一點一點地被實現，像是「擦地板機器人」(掃地機器人)、「機器人汽車」(自駕車)、「空間蠟筆」(3D畫筆)、「萬能製造機」(3D列印機)、「偏光式速成製景相機」(3D列印機)、「拍立得的徽章」(3D列印機)、「免費收看器與接收器」(無人機/空拍機)、「間諜衛星」(無人機/空拍機)、「無人探測飛船」(無人機/空拍機)、「自動電子打字機」(語音輸入)，不過這些令人興奮的科技還是比不上我們夢想著創造出「哆啦A夢」。

從現階段的科技來看，下一步或許會促成未來誕生「智慧城市」(AI City)，儘管離實現真正的機器人似乎還有一段漫長的路要走，但只要我們不斷努力創新技術，那個我們期望的「22世紀」也將離我們不遠。

接下來，就讓我們從機器學習這個領域開始認識機器究竟是如何學習的吧！

* ⚫️ 基本的概念

<blockquote class="bq_setting">從歷史樣本中獲取各樣本之間的關聯性，並以此建立模型(學習)。當遇到新的資料時，系統將能透過模型得出新資料最有可能的結果(預測)。</blockquote>

這是小編接觸機器學習得到的心得。理解機器學習的技術後，大多會被這些技術拉回現實，在偉大的夢想背後，存在許多艱難的問題需要被克服。不過，這些技術背後的原理與人類學習的原理是不是十分相近呢？想想我們人類的腦袋吧！我們有「頭腦」，透過閱讀與觀察「資料」學習知識；相似地，機器則是有「模型」，透過閱讀與觀察「資料」學習知識。

<span class="image featured"><img src="{{ site.baseurl }}/assets/img/20171123/conceptFlowChart.jpg" alt="concept-flow-chart"></span>

在運用機器學習之前，我們應該先了解問題，在運用機器學習的技術之前也是一樣，所以接著我們將說明問題(Problem)與學習(The Machine Learning Method)方面應該注意的概念。

* ⚫️ 問題的特性

<blockquote class="bq_setting">不存在通用的演算法(模型)適用於多個問題(No Free Lunch)，應該熟悉問題與資料集本身，才能設計並訓練出合適的演算法(模型)於該問題以及相似問題上。</blockquote>
這裡要從兩個部分切入進行說明，一個是問題本身，另一個是資料集，這兩者是問題中較為重要的兩個環節，也是我們在實作之前需要事先熟悉的部分。對於問題本身的了解，需要注意的是這個問題最在乎的重點是什麼？例如「檢測病人是否得到重症」這個問題在乎的是檢測(預測)結果不會將重症病人誤判為健康狀態，因為重症病患被誤判為健康的人比健康的人被誤判為重症病患的嚴重性要高出許多，所以在解決這個問題的時候，我們會希望得到重症的病人被判斷為健康的可能性越低越好(期望機率為0)。

至於資料集，需要注意的除了資料集本身資料的內容外，我們也可以去了解或假設資料的分布或特性，這有助於我們挑選、設計或簡化恰當的模型，像是如果資料的分布符合高斯分布，則可以使用高斯機率分布模型逼近(模擬)原始的資料分布。針對每一個問題的特性，如果可以獲得上述內容的資訊，我們就能根據這些線索設計或採用合適的模型作為機器在學習時的原則。

訓練好的模型能用來回答相同的問題，同時這樣的方式也是基於假設未來遇到的同類別資料彼此間差異變化不大的意思(The Smooth Property)。這段落想要帶給各位的觀念就是要先熟悉問題，就像是面對不同的客戶，我們需要依照不同客戶的條件量身打造合適的解決方法一樣；面對不同的問題，我們需要了解問題本身並且熟知來源資料集的特性，才能量身打造合適的預測模型。

* ⚫️ 學習的特性

<blockquote class="bq_setting">演算法(模型)是基於特定假設下被設計出來。面對問題的時候，我們可以從多個演算法(模型)中挑選一個較合適的演算法(模型)應用於問題上。</blockquote>
面對問題，我們會根據發現的特性設計或採用合適的演算法(模型)。機器學習中的問題是個不適定問題(ill-posed problem)，根據每位研究者面對問題時不同的觀察角度或解讀方式，其設計出來或採用的演算法(模型)便不盡相同，甚至在不過分影響效能的情況下，我們也會將問題或資料集應用特定的假設，並以此假設簡化演算法(模型)，換句話說，同樣或相似的問題有許多種解決方法，究竟何種解決方法能有較顯著的效能是不一定的，當然也不能排除研究者未發現較佳方案的可能性，所以在機器學習中，解決方法並不是唯一的，其之間的差別只有效能好與不佳的演算法(模型)。

另外，在機器學習中，如果相同情況下有多個演算法(模型)可以挑選，挑選的原則會盡量以簡單的演算法(模型)為最先考量。挑選演算法(模型)後，我們會透過評估決定該演算法(模型)於問題的效能有多高，這些指標能提供研究者或廠商做為參考的依據。

<hr>

* 🔗️ 參考資料

1. 01.&nbsp;&nbsp;[《哆啦A夢》中的哪些道具已經被實現了？](https://read01.com/5zy0nE.html#.WarDcdQjGUl) from [壹讀](https://read01.com/)  
1. 02.&nbsp;&nbsp;[資料科學的五大迷思](https://buzzorange.com/techorange/2015/08/06/data-science/) from [Tech Orange 科技橘報](https://buzzorange.com/techorange/)  
1. 03.&nbsp;&nbsp;[大數據、資料科學、機器學習、資料探勘、統計方法差在哪？](https://dataholic.wordpress.com/2016/10/18/%E7%AC%AC%E4%B8%80%E7%AF%87%E7%B6%B2%E8%AA%8C%E6%96%87%E7%AB%A0/) from [Dataholic 資料癮](https://dataholic.wordpress.com/)  
1. 04.&nbsp;&nbsp;[物流寄情15：物聯網與雲端運算](http://nmart.pixnet.net/blog/post/47278786-%E7%89%A9%E8%81%AF%E7%B6%B2%E8%88%87%E9%9B%B2%E7%AB%AF%E9%81%8B%E7%AE%97) from [大宅配~ 生活美學 痞客邦](http://nmart.pixnet.net/blog)  
1. 05.&nbsp;&nbsp;[從人工智慧、機器學習到深度學習，你不容錯過的人工智慧簡史](https://www.inside.com.tw/2017/07/10/ai-history) from [INSIDE 硬塞](https://www.inside.com.tw/)  
1. 06.&nbsp;&nbsp;[大數據到底是什麼意思？事實上，它是一種精神！](https://www.inside.com.tw/2017/06/28/big-data) from [INSIDE 硬塞](https://www.inside.com.tw/)  
1. 07.&nbsp;&nbsp;[雲端運算是什麼？Amazon、Google、Microsoft 等大廠爭相佈局，會如何改變人類生活？](https://www.inside.com.tw/2017/06/27/cloud-computing) from [INSIDE 硬塞](https://www.inside.com.tw/)  
1. 08.&nbsp;&nbsp;[【BigData大會搶先看】人工智慧和機器學習有何不同？哈佛AI專家告訴你](http://www.ithome.com.tw/news/101031) from [iThome 硬塞](http://www.ithome.com.tw/)  
1. 09.&nbsp;&nbsp;[圖靈測試](https://zh.wikipedia.org/wiki/%E5%9B%BE%E7%81%B5%E6%B5%8B%E8%AF%95) from [Wikipedia 維基百科](https://zh.wikipedia.org/wiki/Wikipedia:%E9%A6%96%E9%A1%B5)  
1. 10.&nbsp;&nbsp;[人類如何製造智慧？圖靈測試、中文房間論證，及人工智慧發展的三個難題](https://consciousness-popsci.blogspot.tw/2017/03/blog-post_4.html) from [CONSCIOUSNESS 意識物](https://consciousness-popsci.blogspot.tw/)  
1. 11.&nbsp;&nbsp;[Expert system](https://en.wikipedia.org/wiki/Expert_system) from [Wikipedia 維基百科](https://zh.wikipedia.org/wiki/Wikipedia:%E9%A6%96%E9%A1%B5)  