# Cool Quantum BB84 Protocol

Goal 1: Share a secret key  
Goal 2: Eavesdrop  <!-- spacebar twice at end for newline -->  
Goal 3: Noise

## Theory

1) Alice generates random sequence of bits and independently selects corresponding basis, see below. Similarly, Bob selects his measurement bases at random.
2) Alice encodes each bit into a qubit using quantum bits:
    - Rectilinear basis $|0\rangle$ and $1\rangle$
    - Diagonal basis $\frac{1}{\sqrt{2}}(|0\rangle + |1\rangle)$ and $\frac{1}{\sqrt{2}}(|0\rangle - |1\rangle)$
3) Bob measures qubits using his randomly chosen basis. Alice and Bob publicly share their bases choices and discard bits that don't match
4) Can confirm whether there was an eavedropper based on error rates

## Given that there is noise, and there might be an eavesdropper, can we still send a secure message?

Secure here meaning that if there is an eavesdropper, we know, and can therefore abort. But, if we do not know if there is an eavesdropper then the message is not secure. 

## Eavesdropping and QBER

To consider eavesdropping, we invent a new 'person' Eve. Eve generates a basis in the same way as Alice and Bob

