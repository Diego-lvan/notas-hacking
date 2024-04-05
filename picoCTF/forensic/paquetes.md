cat datos.txt | grep UDP | awk '{print $7}' | cut -c2- | grep -v 000

picoCTF{p1LLf3r3d_data_v1a_st3g0}

