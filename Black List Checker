import json #You need to paste in to the Lambda function 

BLACKLISTED_IPS = ["172.16.0.2"] #You can add new ID adress to the black list or download it from some external source

def lambda_handler(event, context):
    ip_to_check = event.get("ip")

    if not ip_to_check:
        return {
            "statusCode": 400,
            "body": json.dumps("Adress is not on the black list") 
        }

    if ip_to_check in BLACKLISTED_IPS:
        result = f"Adress IP {ip_to_check} is on the black list!"
    else:
        result = f"Adress IP {ip_to_check} is safe"

    return {
        "statusCode": 200,
        "body": json.dumps(result)
    }
