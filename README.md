sequenceDiagram
    participant User as 用家
    participant Eye as EyeTrackingManager
    participant Voice as VoiceCommandManager
    participant Controller as ControllerManager
    participant FiveSense as 五感模組
    participant Motion as MotionTrackingManager
    participant AI as AI 建議系統

    User->>Eye: 注視選擇 / 眨眼確認
    Eye->>Controller: 傳送選擇事件
    Controller->>FiveSense: 啟動視覺 / 聽覺 / 觸覺 / 嗅覺 / 味覺
    FiveSense-->>User: 五感回饋

    User->>Voice: 語音指令 (開始 / 返回 / 選擇)
    Voice->>Controller: 傳送語音事件
    Controller->>Motion: 啟動姿勢偵測 / 動作映射
    Motion-->>AI: 傳送體感數據
    AI-->>User: 提供智能建議 (例如「保持平衡」)

