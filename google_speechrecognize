import speech_recognition as sr

def recognize_speech():
    # 初始化识别器
    r = sr.Recognizer()
    
    with sr.Microphone() as source:
        print("请说话...")
        # 记录音频
        audio = r.listen(source)
        
    try:
        # 使用Google Web Speech API进行识别，它对中英文混合语音有较好的支持
        text = r.recognize_google(audio, language='zh-CN,en-US')
        return text
    except sr.UnknownValueError:
        return "无法识别你的语音"
    except sr.RequestError as e:
        return f"无法获取结果; 错误详情: {error}"

if __name__ == "__main__":
    message = recognize_speech()
    print(message)
