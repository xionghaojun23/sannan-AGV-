[deepseek_json_20251113_e46db7.json](https://github.com/user-attachments/files/23515175/deepseek_json_20251113_e46db7.json)
{
    "assetModel": {
        "assetId": "DT-001",
        "name": "一号干式变压器",
        "description": "为主生产线供电的干式变压器",
        "isa95Hierarchy": {
            "enterprise": "automagic",
            "site": "Hangzhou_Xiaoshan",
            "area": "Area_PowerDistribution",
            "processCell": "PC_Substation",
            "unit": "Unit_Substation_A"
        },
        "type": "DryTypeTransformer",
        "specifications": {
            "ratedCapacity": "1000kVA",
            "primaryVoltage": "10kV",
            "secondaryVoltage": "400V",
            "insulationClass": "F",
            "coolingType": "AN"
        },
        "energyParameters": {
            "meterId": "EM-TX-001",
            "energyType": "electricity",
            "unitOfMeasure": "kWh",
            "costCenter": "CC-MainProduction-01"
        }
    },
    "telemetry": {
        "timestamp": "2024-05-17T10:30:45.123Z",
        "values": {
            "temperature_C": 78.5,
            "load_percentage": 85.2,
            "inputVoltage_V": 10050,
            "outputVoltage_V": 398.2,
            "current_A": 1205.7,
            "powerFactor": 0.92
        },
        "status": {
            "health": "error",
            "cooling_fan_running": true,
            "alarm_status": "trigger"
        }
    },
    "metadata": {
        "version": "1.0",
        "messageType": "combined_asset_telemetry"
    },
    // ===== 测试代码开始 =====
    "testCode": {
        "testScenario": "错误状态验证",
        "testId": "TEST-001",
        "expectedBehavior": "当health为error时，系统应触发警报",
        "testData": {
            "simulatedTemperature": 95.0,
            "simulatedLoad": 95.5,
            "testTimestamp": "2024-05-17T11:00:00.000Z"
        },
        "validationRules": [
            "温度超过90度应触发高温警报",
            "负载超过90%应触发过载警报",
            "health状态为error时应记录故障日志"
        ]
    }
    // ===== 测试代码结束 =====
}
