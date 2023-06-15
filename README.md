# r5-mlops
# R5 MLOps - General Overview

## Main points for consideration:

**Inference Scalability:**
- Container platforms for efficient scaling: Kubernetes.
- Deploy models as Kubernetes pods or EC2 instances.
- Use AWS Auto Scaling for efficent resources use.
- Distribute incoming requests with AWS Elastic Load Balancer.

**Machine Learning CI/CD:**
- Implement automated CI/CD pipelines for model deployment and versioning.
- Version control systems: Git.
- Infrastructure definition: AWS CloudFormation or Terraform.
- Define and include include automated testing and integration tests.
- CI/CD implementation: Jenkins or AWS CodePipeline.

**Model Validation (Data Drift and Model Drift):**
- Data drift and model drift monitorin and detection: AWS SageMaker Model Monitor / Evidently 
- Compare data distributions for drift detection.
- Trigger retraining based on model drift performance metrics.

**Data Versioning:**
- Define data versioning protocols for consistency and traceability.
- Store data in AWS S3 or AWS Glue Data Catalog.
- Ideally, trained model versions should have an association with data versions.

**Model Continuous Training:**
- Implement continuous training to improve models over time that are linked with the model validation triggers.
- Set up regular retraining schedules based on business needs (Independent from Model Validation).
- This could be integrated into the CI/CD pipeline.

**Security and Compliance:**
- Implement security measures for models, data, and infrastructure.
- Apply access controls, encryption, and data privacy.

**Logging and Monitoring:**
- Logging for inference requests, errors, and performance: AWS CloudWatch.

