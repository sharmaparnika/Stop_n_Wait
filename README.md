# Stop n Wait Protocol

AIM: Implementation of Stop and Wait Protocol

## ALGORITHM:

Sender:

    Step1: sequence ß 0
    Step2: Accept new packet and assign sequence to it.
    Step3: Send packet sequence with sequence number sequence.
    Step4: Set timer for recently sent packets.
    Step5: If error free acknowledgment from receiver and NextFrameExpected -> sequence then sequence -> NextFrameExpected.
    Step6: If time out then go to step3.
    Step7: Stop.

Receiver:

    Step1: Start.
    Step2: NextFrameExpected <- 0, repeat steps 3 forever.
    Step3: If error-free frame received and sequence= NextFrameExpected, then pass packet to higher layer and NextFrameExpected <- NextFrameExpected+1(modulo 2).
    Step4: Stop.

## Sender Snapshot:

![image](https://user-images.githubusercontent.com/73773202/156939144-4eb95db7-b3b2-4646-bc93-e56d9d8322b7.png)

## Receiver Snapshot:

![image](https://user-images.githubusercontent.com/73773202/156939158-2f0db4e4-b7c1-44e3-91c4-6c4dfd974803.png)

---
