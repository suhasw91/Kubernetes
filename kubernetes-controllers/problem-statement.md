Consider a scenario where the product/application team you're working with is now
ready to put their application in production and they need your help to deploy it in a
replicated and reliable manner. For the scope of this exercise, consider the following
requirements for the application:

• The default number of replicas should be 6.
• For simplicity, you can use the nginx image for the container running in
the Pod.
• Make sure all the Pods have the following two labels with corresponding value:

                        activity=first
                        
• The update strategy for the Deployment should be RollingUpdate. At worst,
no more than half of the Pods can be down, and similarly, at no point should
there be more than 150% of the desired count of Pods.

The following are the high-level steps to perform this activity:
1. Create a namespace for this activity.
2. Write the Deployment configuration. Ensure that it meets all the requirements
that are specified.
3. Create the Deployment using the configuration from the previous step.
4. Verify that six Pods were created by the Deployment.