# AWS Architecture Diagram - AI-Powered Pulmonary Care System

## 🎯 Overview

This directory contains the professional AWS architecture diagram for the AI-Powered Pulmonary Care System, designed for the **AI for Bharat AWS Hackathon** professional track submission.

## 📁 Files

- **`aws-architecture-diagram.svg`** - High-quality vector diagram (1600x1200px)
- **`convert_to_png.py`** - Script to convert SVG to PNG format
- **`generate_diagram.py`** - Alternative diagram generator
- **`create_clear_aws_diagram.py`** - Matplotlib-based generator
- **`README.md`** - This documentation file

## 🏗️ Architecture Components

### **Edge & Gateway Services**
- **🌐 AWS IoT Core**: Device registry, MQTT messaging, <100ms processing
- **🚪 API Gateway**: REST APIs, authentication, rate limiting
- **⚡ AWS Lambda**: Serverless compute, auto-scaling, event-driven
- **🌊 Amazon Kinesis**: Real-time streaming, 10K+ messages/second

### **Storage Services**
- **🗄️ DynamoDB**: Real-time health data, 5 tables + GSI, millisecond latency
- **🪣 Amazon S3**: Historical data, ML artifacts, intelligent lifecycle
- **🗃️ Amazon RDS**: Provider data, HIPAA audit logs, multi-AZ HA

### **AI/ML Services**
- **🧠 SageMaker**: Pulmonary prediction models, <1s inference
- **🤖 Amazon Lex**: AI chatbot, multi-language NLP, <3s response
- **🗣️ NLP Services**: Comprehend, Translate, Transcribe, medical entities

### **Security & Monitoring**
- **🔒 Comprehensive Security**: KMS encryption, Cognito auth, CloudTrail audit
- **📊 Monitoring**: CloudWatch metrics, SNS alerts, emergency response
- **✅ Compliance**: HIPAA, data retention, audit trails

## 🎯 Key Performance Metrics

| Metric | Target | Description |
|--------|--------|-------------|
| **Processing Latency** | <100ms | IoT Core to DynamoDB |
| **ML Inference** | <1 second | SageMaker endpoint response |
| **Alert Response** | <5 seconds | Critical health alerts |
| **Chatbot Response** | <3 seconds | Multi-language AI responses |
| **Concurrent Users** | 1M+ | Supported user load |
| **Availability** | 99.99% | Uptime SLA with multi-AZ |
| **Data Processing** | 10K+/sec | Messages per second |

## 🌍 Multi-Language Support

- **Indian Languages**: Hindi, Tamil, Telugu, Bengali, Marathi
- **International**: English with regional dialects
- **Features**: Voice recognition, synthesis, cultural context awareness

## 🚨 Emergency Response Integration

- **Automatic Detection**: SpO2 <90%, respiratory distress, multi-parameter alerts
- **Response Time**: <5 seconds from detection to notification
- **Integration**: Emergency services, healthcare providers, family members
- **Data Sharing**: Real-time vitals, location, medical history

## 📊 Data Flow Architecture

```
Wearable Device (1Hz) → IoT Core → Lambda → DynamoDB (Real-time)
                                      ↓
                                  Kinesis → S3 (Historical)
                                      ↓
                              SageMaker → Predictions
                                      ↓
                                 Lex → AI Responses
                                      ↓
                                 SNS → Alerts
```





# rsvg-convert
rsvg-convert -d 300 -p 300 -o diagram.png aws-architecture-diagram.svg
```
