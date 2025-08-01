<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "bbce3572338711aeab758506379ab716",
  "translation_date": "2025-07-12T13:46:00+00:00",
  "source_file": "11-mcp/README.md",
  "language_code": "hi"
}
-->
# Lesson 11: Model Context Protocol (MCP) Integration

## Model Context Protocol (MCP) का परिचय

Model Context Protocol (MCP) एक अत्याधुनिक फ्रेमवर्क है जिसे AI मॉडल्स और क्लाइंट एप्लिकेशन के बीच इंटरैक्शन को मानकीकृत करने के लिए डिज़ाइन किया गया है। MCP AI मॉडल्स और उन एप्लिकेशन के बीच एक पुल का काम करता है जो उनका उपयोग करते हैं, जिससे मॉडल के अंतर्निहित कार्यान्वयन की परवाह किए बिना एक समान इंटरफ़ेस मिलता है।

MCP के मुख्य पहलू:

- **मानकीकृत संचार**: MCP एप्लिकेशन और AI मॉडल्स के बीच संवाद के लिए एक सामान्य भाषा स्थापित करता है
- **बेहतर संदर्भ प्रबंधन**: AI मॉडल्स को संदर्भित जानकारी कुशलतापूर्वक पास करने की अनुमति देता है
- **क्रॉस-प्लेटफ़ॉर्म संगतता**: C#, Java, JavaScript, Python, और TypeScript सहित विभिन्न प्रोग्रामिंग भाषाओं में काम करता है
- **सहज एकीकरण**: डेवलपर्स को विभिन्न AI मॉडल्स को अपनी एप्लिकेशन में आसानी से एकीकृत करने में सक्षम बनाता है

MCP AI एजेंट विकास में विशेष रूप से मूल्यवान है क्योंकि यह एजेंट्स को विभिन्न सिस्टम और डेटा स्रोतों के साथ एकीकृत प्रोटोकॉल के माध्यम से इंटरैक्ट करने की अनुमति देता है, जिससे एजेंट अधिक लचीले और शक्तिशाली बनते हैं।

## सीखने के उद्देश्य
- MCP क्या है और AI एजेंट विकास में इसकी भूमिका को समझना
- GitHub इंटीग्रेशन के लिए MCP सर्वर सेटअप और कॉन्फ़िगर करना
- MCP टूल्स का उपयोग करके मल्टी-एजेंट सिस्टम बनाना
- Azure Cognitive Search के साथ RAG (Retrieval Augmented Generation) को लागू करना

## आवश्यकताएँ
- Python 3.8+
- Node.js 14+
- Azure सब्सक्रिप्शन
- GitHub खाता
- Semantic Kernel की बुनियादी समझ

## सेटअप निर्देश

1. **पर्यावरण सेटअप**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

2. **Azure सेवाओं को कॉन्फ़िगर करें**
   - Azure Cognitive Search संसाधन बनाएं
   - Azure OpenAI सेवा सेटअप करें
   - `.env` में पर्यावरण चर कॉन्फ़िगर करें

3. **MCP सर्वर सेटअप**
   ```bash
   npm install -g @modelcontextprotocol/server-github
   ```

## प्रोजेक्ट संरचना

```
11-mcp/
├── code_samples/
│   └── github-mcp/
│       ├── app.py              # Main application
│       ├── event-descriptions.md  # Event data
│       └── MCP_SETUP.md        # Setup guide
├── README.md
└── requirements.txt
```

## मुख्य घटक

### 1. मल्टी-एजेंट सिस्टम
- GitHub एजेंट: रिपॉजिटरी विश्लेषण
- Hackathon एजेंट: प्रोजेक्ट सिफारिशें
- Events एजेंट: टेक इवेंट सुझाव

### 2. Azure इंटीग्रेशन
- इवेंट इंडेक्सिंग के लिए Cognitive Search
- एजेंट इंटेलिजेंस के लिए Azure OpenAI
- RAG पैटर्न का कार्यान्वयन

### 3. MCP टूल्स
- GitHub रिपॉजिटरी विश्लेषण
- कोड निरीक्षण
- मेटाडेटा निष्कर्षण

## कोड वॉकथ्रू

यह उदाहरण दिखाता है:
1. MCP सर्वर इंटीग्रेशन
2. मल्टी-एजेंट ऑर्केस्ट्रेशन
3. Azure Cognitive Search इंटीग्रेशन
4. RAG पैटर्न का कार्यान्वयन

मुख्य विशेषताएं:
- रियल-टाइम GitHub रिपॉजिटरी विश्लेषण
- बुद्धिमान प्रोजेक्ट सिफारिशें
- Azure Search के साथ इवेंट मिलान
- Chainlit के साथ स्ट्रीमिंग प्रतिक्रियाएं

## सैंपल चलाना

विस्तृत सेटअप निर्देश और अधिक जानकारी के लिए, [Github MCP Server Example README](./code_samples/github-mcp/README.md) देखें।

1. MCP सर्वर शुरू करें:
   ```bash
   npx @modelcontextprotocol/server-github
   ```

2. एप्लिकेशन लॉन्च करें:
   ```bash
   chainlit run app.py -w
   ```

3. इंटीग्रेशन का परीक्षण करें:
   ```
   Example query: "Analyze repositories for username: <github_username>"
   ```

## समस्या निवारण

सामान्य समस्याएं और समाधान:
1. MCP कनेक्शन समस्याएं
   - सुनिश्चित करें कि सर्वर चल रहा है
   - पोर्ट उपलब्धता जांचें
   - GitHub टोकन की पुष्टि करें

2. Azure Search समस्याएं
   - कनेक्शन स्ट्रिंग्स सत्यापित करें
   - इंडेक्स की उपस्थिति जांचें
   - दस्तावेज़ अपलोड की पुष्टि करें

## अगले कदम
- अतिरिक्त MCP टूल्स का अन्वेषण करें
- कस्टम एजेंट्स लागू करें
- RAG क्षमताओं को बढ़ाएं
- और अधिक इवेंट स्रोत जोड़ें

## संसाधन
- [MCP for Beginners](https://aka.ms/mcp-for-beginners)  
- [MCP Documentation](https://github.com/microsoft/semantic-kernel/tree/main/python/semantic-kernel/semantic_kernel/connectors/mcp)
- [Azure Cognitive Search Docs](https://learn.microsoft.com/azure/search/)
- [Semantic Kernel Guides](https://learn.microsoft.com/semantic-kernel/)

**अस्वीकरण**:  
यह दस्तावेज़ AI अनुवाद सेवा [Co-op Translator](https://github.com/Azure/co-op-translator) का उपयोग करके अनुवादित किया गया है। जबकि हम सटीकता के लिए प्रयासरत हैं, कृपया ध्यान दें कि स्वचालित अनुवादों में त्रुटियाँ या अशुद्धियाँ हो सकती हैं। मूल दस्तावेज़ अपनी मूल भाषा में ही अधिकारिक स्रोत माना जाना चाहिए। महत्वपूर्ण जानकारी के लिए, पेशेवर मानव अनुवाद की सलाह दी जाती है। इस अनुवाद के उपयोग से उत्पन्न किसी भी गलतफहमी या गलत व्याख्या के लिए हम जिम्मेदार नहीं हैं।