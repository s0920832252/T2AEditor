# T2AEditor
### 語音轉文字應用開發平台(https://stt.itri.org.tw/development/manual.php)
T2A (Text2Action) 語音指令編輯器，是為了工研院語音聲動雲 STT@ITRI之應用
程式開發者，所提供的一個簡易直覺的語音指令編輯與上傳工具。這個工具的主要
特點如下：
1. 採用微軟 Excel 作為客戶端編輯工具。每個.xlsm 檔可設計一到多個 Group，每個 Group 代表一種句型，有自己獨特的名稱 (Group_ID)。
2. 每個 Group 句型由一到兩個 Slot 組成，每個 Slot 可包含一到多個常數或變數：
> 1. 每個常數是一段可被辨識之話語字串。
> 2. 每個變數是另一個已定義的 Group_ID：藉由 Group 內又可引用包含其他Group，就可以設計出具有樹狀語意結構的複雜句型。
3. 透過語音指令的設計編寫，除了定義語音辨識器可辨識的話語內容字串外，同時也定義了此話語內容的句型語意類別群組 Group_ID。
> 1. 因此當使用此工具所設計的語音指令，在應用時針對每一句輸入語音，STT@ITRI將會輸出：
>> 1. 辨識出來的整段文句字串，以及該文句句型所屬的指令集 Group_ID。
>> 2. 文句中每個 Slot 常數字串，以及該常數字串之 Slot 所屬的 Group_ID。
> 2. 這也是為何此工具軟體稱為 T2A 語音指令編輯器，因為系統除了輸出文字 (Text) 以外，也同時輸出該文字的語意類別群組 Group_ID，而據此應
用程式就能進行必要的回應動作 (Action)。
