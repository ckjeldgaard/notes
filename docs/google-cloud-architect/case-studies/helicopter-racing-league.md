---
sidebar_position: 2
---

# Helicopter Racing League

- Global sports league (i.e. lots of regional focus)
- World championships **and** regional leagues
- Offers paid streaming service with predictions (uptime is therefore important)

## Concerns

- Migrate to new platform
- Use AI & ML
- New regions
- Stream + record closer to users to keep latency down

## Existing

- Already in a cloud
- Object storage
- VM video encode/transcode at the racetracks
- Running predictions using TensorFlow on other VMs in the cloud (moving forward, use **TensorFlow Extended** and **Vertex AI Workbench** notebooks as they support TensorFlow)

## Business requirements

- Models to partners
- Increase telemetry
- Measure fan engagement (AI and ML models)
- Increase concurrent viewers
- Ensure compliance
- Merchandise (some e-commerce app or connection to one)
- Minimize operational complexity (use **Storage Transfer Service** to move content on GCP in a cost-effective manner)

## Technical requirements

- Prediction throughput
- Reduce latency
- Transcoding performance **(vertically scale up their VM's on the processing side - i.e. "add more compute to one machine")**
- Realtime analysis (streaming data and data pipeline)
- Batch

## Summary

- Predictions with AI and ML. Use **Natural Language API** to measure fan engagement
- Extending reach and market
- Lots of data in near-real time
