# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output

```
14:39:38] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
[14:39:38] DEBUG | Sending PUBLISH (d0, q1, r0, m1), 'b'test/qos/6510301011/temperature'', ... (5 bytes)
[14:39:38] PUBLISH REQUESTED | SID=6510301011 | temperature=26.37 | QoS=1 | msgid=1
[14:39:38] DEBUG | Sending PUBLISH (d0, q1, r0, m2), 'b'test/qos/6510301011/humidity'', ... (5 bytes)
[14:39:38] PUBLISH REQUESTED | SID=6510301011 | humidity=58.01 | QoS=1 | msgid=2
[14:39:38] DEBUG | Sending PUBLISH (d0, q1, r0, m3), 'b'test/qos/6510301011/pressure'', ... (6 bytes)
[14:39:38] PUBLISH REQUESTED | SID=6510301011 | pressure=1010.7 | QoS=1 | msgid=3
[14:39:38] DEBUG | Sending PUBLISH (d0, q1, r0, m4), 'b'test/qos/6510301011/fan_speed'', ... (1 bytes)
[14:39:38] PUBLISH REQUESTED | SID=6510301011 | fan_speed=0 | QoS=1 | msgid=4
[14:39:38] DEBUG | Received CONNACK (0, 0)
[14:39:38] DEBUG | Received PUBACK (Mid: 1)
[14:39:38] PUBLISHED | msgid=1
[14:39:38] DEBUG | Received PUBACK (Mid: 2)
[14:39:38] PUBLISHED | msgid=2
[14:39:38] DEBUG | Received PUBACK (Mid: 3)
[14:39:38] PUBLISHED | msgid=3
[14:39:38] DEBUG | Received PUBACK (Mid: 4)
[14:39:38] PUBLISHED | msgid=4
```

## Subscriber_qos.py Output

```
/Users/parichaya23icloud.com/Desktop/Iot-class-2025-gateway/app/subscriber_wildcard.py:37: DeprecationWarning: Callback API version 1 is deprecated, update to latest version
  client = mqtt.Client()
[14:42:13] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
[14:42:13] DEBUG | Received CONNACK (0, 0)
[14:42:13] Connected with result code 0
[14:42:13] DEBUG | Sending SUBSCRIBE (d0, m1) [(b'test/qos/6510301011/#', 2)]
[14:42:13] SUBSCRIBED to test/qos/6510301011/# with QoS=2
[14:42:13] DEBUG | Received SUBACK

```