# Scan Surprise

```python
import cv2
from pyzbar.pyzbar import decode
import numpy as np

# Read the image file
image = cv2.imread('flag.png')

# Decode the QR code
qr_codes = decode(image)

# Loop through all detected QR codes
for qr_code in qr_codes:
    qr_data = qr_code.data.decode('utf-8')
    qr_type = qr_code.type
    print(f"Decoded {qr_type} QR code: {qr_data}")

    # Draw a rectangle around the QR code
    points = qr_code.polygon
    if len(points) == 4:
        # Convert points to an array of coordinates for cv2.polylines
        pts = np.array([(point.x, point.y) for point in points], dtype=np.int32)
        pts = pts.reshape((-1, 1, 2))  # Reshape for cv2.polylines
        cv2.polylines(image, [pts], isClosed=True, color=(0, 255, 0), thickness=2)

# Display the image with the QR code highlighted
cv2.imshow('QR Code Scanner', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


**Answer: `picoCTF{p33k_@_b00_7843f77c}`**