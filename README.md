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

 ![alt=""](Images/terminal-run-streamlit.png)   


 ![alt=""](Images/streamlit1.png)


 ![alt=""](Images/streamlit2.png)


 ![alt=""](Images/streamlit3.png)


