# Secure Sight 

## Inspiration
In times of emergency, every second counts, and unfortunately, not all victims can reach out safely or quickly enough to call for help. This inspired us to create Secure Sight, a proactive and accessible security solution that leverages machine learning to detect potential threats in real-time and alert security personnel. We wanted to build a tool that would empower individuals to anonymously report incidents with supporting evidence, bridging the gap between threat detection and law enforcement.

## What it does
Secure Sight uses a machine learning model to analyze live CCTV camera feeds, detecting the presence of weapons in real-time. If a weapon is detected, the system uploads the evidence to an Amazon S3 bucket to maintain data integrity and automatically sends an alert to security admins via WhatsApp, using the Twilio API. The alert message contains the weapon detection details, location, and an image to validate the detection as a true positive. Secure Sight also features a web interface that includes anonymous crime reporting, allowing users to submit incident descriptions and evidence images without any personal identification. This layer of anonymity encourages more people to report incidents without fear of police scrutiny.

## How we built it
We built Secure Sight using a blend of machine learning and web technologies:
- **Machine Learning Model**: Our model processes CCTV camera feeds to detect weapons in real-time. We fine-tuned the model to optimize detection rates, improving its ability to recognize weapons accurately in diverse scenarios.
- **AWS S3 for Storage**: When a weapon is detected, the evidence is securely stored in an S3 bucket, ensuring that the data is both secure and readily accessible for security personnel.
- **Twilio API for Notifications**: To notify admins of potential threats, we implemented the Twilio API, allowing alerts to be sent via WhatsApp without requiring the admin to download additional applications.
- **Web Interface with Vanilla JavaScript**: We developed a simple, user-friendly web interface that showcases Secure Sight’s features, including an anonymous crime reporting system. This interface was built with vanilla JavaScript, making it efficient, lightweight, and easy to deploy via GitHub Pages.

## Challenges we ran into
Building Secure Sight presented several challenges:
- **Model Accuracy**: Initially, the detection model struggled with accuracy, especially in distinguishing weapons from other objects. We addressed this by further fine-tuning and testing the model, which significantly improved detection reliability.
- **API Integration with Vanilla JavaScript**: Integrating the Twilio API and uploading images to S3 solely using vanilla JavaScript proved challenging. We had to refine our approach multiple times to achieve smooth functionality.
- **Anonymous Reporting Feature**: Creating a seamless, anonymous reporting feature required careful attention to design to ensure user privacy while maintaining the reliability of the information sent.

## Accomplishments that we're proud of
We’re proud of building a comprehensive, end-to-end solution that takes immediate action upon threat detection by alerting admins via WhatsApp. The anonymous reporting feature is another major accomplishment, making it possible for anyone to report incidents discreetly, which we hope will encourage greater community involvement in reporting suspicious activities.

## What we learned
Throughout this project, we expanded our knowledge in various areas:
- **AWS S3**: We gained experience with AWS S3 for secure data storage, learning how to efficiently manage and retrieve stored images.
- **Twilio API**: This was our first time using the Twilio API to send WhatsApp notifications, and we learned how to construct and send requests effectively.
- **Machine Learning in Real-World Applications**: Developing a model capable of analyzing camera feeds in real-time helped us understand the challenges and optimizations needed for real-world machine learning applications.

## What's next for Secure Sight
Our goal is to enhance Secure Sight by further improving its accuracy while optimizing it to run efficiently on edge devices, such as low-power systems or IoT devices, making it a cost-effective solution that can be deployed widely with minimal latency. By refining its edge capability, we aim to make Secure Sight accessible to schools, businesses, and public spaces, providing a proactive security tool that could potentially prevent crimes before they happen.
