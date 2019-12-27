# SCSys
# User
registerUserTask(PARAM)
  PARAM
    SENSING: 시스템에 sensing 작업이 포함된 task를 등록
    PROCESS_COMM: 시스템에 processing 및 communicating 작업이 포함된 task를 등록

# System - Energy Management
getEnergyChanged(t)
  앞으로 t 동안 사용할 수 있는 에너지 반환
startSCService() / startHarvService()
  Supercapacitor / Harvesting 정보를 관리하는 Service
getSCEnergy()
  Time, Voltage 정보를 고려한 Supercapacitor의 정확한 SoC 측정 및 반환
getSCVoltage()
  Supercapacitor의 voltage 반환
getHarvEnergy()
  model data를 이용해 harvesting 에너지량을 예측
getModelData()
  EWMA 등 harvesting 환경의 model data

# System - Elastic Task Management
determineWorkload()
  Processing and Communicating task를 얼마나 실행할지 결정
determineDutyCycle()
  Duty cycle 결정
