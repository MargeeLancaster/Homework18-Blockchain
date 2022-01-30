# Homework18-Blockchain
## PyChain Ledger 
Build a blockchain-based ledger system, complete with a user-friendly web interface

Update the provided Python file, which already contains the basic `PyChain`:

1. Create a new data class named `Record`. It a blueprint for the financial transaction records that the ledger blocks will store.

2. Modify the existing `Block` data class to store `Record` data.

3. Add Relevant User Inputs to the Streamlit interface.

4. Test the PyChain Ledger by Storing Records.

## Step 1 - Create new data class named 'Record"

@dataclass

class Record:

    sender: str
    receiver: str
    amount: float

## Step 2 - Modify existing 'Block data class to store 'Record' data 

class: Block

    record: Record

## Step 3 - Add relevent User Imputs to the Streamlit Interface

sender = st.text_input("Sender")

receiver = st.text_input("Receiver")  
amount = st.text_input("Amount")  

new_block = Block(

        record=Record(sender, receiver, amount),
        # data=input_data,
        creator_id=42,
        prev_hash=prev_block_hash
    )

    pychain.add_block(new_block)
    st.balloons()

 ## Step 4 - Test the PyChain Ledger by Storing Records

 ![Terminal Run Streamlit](./Images/terminal-run-streamlit.png)   


 ![Streamlit imputing Records](./Images/streamlit1.png)


 ![PyChain Transaction Record](./Images/streamlit2.png)


 ![Validation Transaction](./Images/streamlit3.png)

 ## How it Works
There are three user imputs:

* Sender
* Receiver
* Amount

This information is store in a dictionary and is stored as a Record in the Blockchain.  Each block contains intormation about the transaction along with the time of the tranaction, id of the person minting the transaction, the hash of the previous tranaction and the nonce.  These transactions are then validated to confirm that it is legitimate.


 


