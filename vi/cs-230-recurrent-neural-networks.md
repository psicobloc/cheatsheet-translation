**Recurrent Neural Networks translation** [[webpage]](https://stanford.edu/~shervine/teaching/cs-230/cheatsheet-recurrent-neural-networks)

<br>

**1. Recurrent Neural Networks cheatsheet**

&#10230; Cheatsheet về mạng neural hồi quy

<br>


**2. CS 230 - Deep Learning**

&#10230; CS 230 - Deep Learning

<br>


**3. [Overview, Architecture structure, Applications of RNNs, Loss function, Backpropagation]**

&#10230; [Tổng quan, Kết cấu kiến trúc, Ứng dụng của RNNs, Hàm mất mát, Lan truyền ngược]

<br>


**4. [Handling long term dependencies, Common activation functions, Vanishing/exploding gradient, Gradient clipping, GRU/LSTM, Types of gates, Bidirectional RNN, Deep RNN]**

&#10230; [Xử lí các phụ thuộc dài hạn, Các hàm kích hoạt phổ biến, Vanishing/exploding gradient, Gradient clipping, GRU/LSTM, Các loại cổng, RNN hai chiều, RNN xâu]

<br>


**5. [Learning word representation, Notations, Embedding matrix, Word2vec, Skip-gram, Negative sampling, GloVe]**

&#10230; [Học từ đại diện, Ký hiệu, Ma trận nhúng, Word2vec, Skip-gram, Lấy mẫu âm, GloVe]

<br>


**6. [Comparing words, Cosine similarity, t-SNE]**

&#10230; [So sánh các từ, Độ tương đồng Cosine, t-SNE]

<br>


**7. [Language model, n-gram, Perplexity]**

&#10230; [Hô hình ngôn ngữ, n-gram, Perplexity]

<br>


**8. [Machine translation, Beam search, Length normalization, Error analysis, Bleu score]**

&#10230; [Dịch máy, Tìm kiếm Beam, Chuẩn hoá độ dài, Phân tích lỗi, Bleu score]

<br>


**9. [Attention, Attention model, Attention weights]**

&#10230; [Attention, Mô hình Attention, Trọng số Attention]

<br>


**10. Overview**

&#10230; Tổng quan

<br>


**11. Architecture of a traditional RNN ― Recurrent neural networks, also known as RNNs, are a class of neural networks that allow previous outputs to be used as inputs while having hidden states. They are typically as follows:**

&#10230; Kiến trúc của một mạng RNN truyền thống - Các mạng neural hồi quy, còn được biến đến như là RNNs, là một lớp của mạng neural cho phép đầu ra được sử dụng như đầu vào trong khi có các trạng thái ẩn. Thông thường là như sau:

<br>


**12. For each timestep t, the activation a<t> and the output y<t> are expressed as follows:**

&#10230; Tại mỗi bước t, giá trị kích hoạt a<t> và đầu ra y<t> được biểu diễn như sau:

<br>


**13. and**

&#10230; và

<br>


**14. where Wax,Waa,Wya,ba,by are coefficients that are shared temporally and g1,g2 activation functions.**

&#10230; với Wax,Waa,Wya,ba,by là các hệ số được chia sẻ tạm thời và g1,g2 là các hàm kích hoạt.

<br>


**15. The pros and cons of a typical RNN architecture are summed up in the table below:**

&#10230; Ưu và nhược điểm của một kiến trúc RNN thông thường được tổng kết ở bảng dưới đây:

<br>


**16. [Advantages, Possibility of processing input of any length, Model size not increasing with size of input, Computation takes into account historical information, Weights are shared across time]**

&#10230; [Ưu điểm, Khả năng xử lí đầu vào với bất kì độ dài nào, Kích cỡ mô hình không tăng theo kích cỡ đầu vào, Quá trình tính toán sử dụng các thông tin cũ, Trọng số được chia sẻ trong suốt thời gian]

<br>


**17. [Drawbacks, Computation being slow, Difficulty of accessing information from a long time ago, Cannot consider any future input for the current state]**

&#10230; [Hạn chế, Tính toán chậm, Khó để truy cập các thông tin từ một khoảng thời gian dài trước đây, Không thể xem xét bất kì đầu vào sau này nào cho trạng thái hiện tại]

<br>


**18. Applications of RNNs ― RNN models are mostly used in the fields of natural language processing and speech recognition. The different applications are summed up in the table below:**

&#10230; Ứng dụng của RNNs - Các mô hình RNN hầu như được sử dụng trong lĩnh vực xử lí ngôn ngữ tự nhiên và ghi nhận tiếng nói. Các ứng dụng khác được tổng kết trong bảng dưới đây:

<br>


**19. [Type of RNN, Illustration, Example]**

&#10230; [Các loại RNN, Hình minh hoạ, Ví dụ]

<br>


**20. [One-to-one, One-to-many, Many-to-one, Many-to-many]**

&#10230; [Một-Một, Một-nhiều, Nhiều-một, Nhiều-nhiều]

<br>


**21. [Traditional neural network, Music generation, Sentiment classification, Name entity recognition, Machine translation]**

&#10230; [Mạng neural truyền thống, Sinh nhạc, Phân loại ý kiến, Ghi nhận thực thể tên, Dịch máy]

<br>


**22. Loss function ― In the case of a recurrent neural network, the loss function L of all time steps is defined based on the loss at every time step as follows:**

&#10230; Hàm mất mát - Trong trường hợp của mạng neural hồi quy, hàm mất mát L của tất cả các bước thời gian được định nghĩa dựa theo mất mát ở mọi thời điểm như sau:

<br>


**23. Backpropagation through time ― Backpropagation is done at each point in time. At timestep T, the derivative of the loss L with respect to weight matrix W is expressed as follows:**

&#10230; Lan truyền ngược theo thời gian - Lan truyền ngược được hoàn thành ở mỗi một thời điểm cụ thể. Ở bước T, đạo hàm của hàm mất mát L với ma trận trọng số W được biểu diễn như sau:

<br>


**24. Handling long term dependencies**

&#10230; Xử lí phụ thuộc dài hạn

<br>


**25. Commonly used activation functions ― The most common activation functions used in RNN modules are described below:**

&#10230; Các hàm kích hoạt thường dùng - Các hàm kích hoạt thường dùng trong các modules RNN được miêu tả như sau:

<br>


**26. [Sigmoid, Tanh, RELU]**

&#10230; [Sigmoid, Tanh, RELU]

<br>


**27. Vanishing/exploding gradient ― The vanishing and exploding gradient phenomena are often encountered in the context of RNNs. The reason why they happen is that it is difficult to capture long term dependencies because of multiplicative gradient that can be exponentially decreasing/increasing with respect to the number of layers.**

&#10230; Vanishing/exploding gradient - Hiện tượng vanishing và exploding gradient thường gặp trong ngữ cảnh của RNNs. Lí do tại sao chúng thường xảy ra đó là khó để có được sự phụ thuộc dài hạn vì multiplicative gradient có thể tăng/giảm theo hàm mũ tương ứng với số lượng các tầng.

<br>


**28. Gradient clipping ― It is a technique used to cope with the exploding gradient problem sometimes encountered when performing backpropagation. By capping the maximum value for the gradient, this phenomenon is controlled in practice.**

&#10230; Gradient clipping - Là một kĩ thuật được sử dụng để giải quyết vấn đề exploding gradient xảy ra khi thực hiện lan truyền ngược. Bằng việc giới hạn giá trị lớn nhất cho gradient, hiện tượng này sẽ được kiểm soát trong thực tế.

<br>


**29. clipped**

&#10230; clipped

<br>


**30. Types of gates ― In order to remedy the vanishing gradient problem, specific gates are used in some types of RNNs and usually have a well-defined purpose. They are usually noted Γ and are equal to:**

&#10230; Các loại cổng - Để giải quyết vấn đề vanishing gradient, các cổng cụ thể được sử dụng trong một vài loại RNNs và thường có mục đích rõ ràng. Chúng thường được kí hiệu là Γ và bằng với:

<br>


**31. where W,U,b are coefficients specific to the gate and σ is the sigmoid function. The main ones are summed up in the table below:**

&#10230; Với W, U, b là các hệ số của một cổng và σ là hàm sigmoid. Các loại chính được tổng kết ở bảng dưới đây:

<br>


**32. [Type of gate, Role, Used in]**

&#10230; [Loại cổng, Vai trò, Được sử dụng trong]

<br>


**33. [Update gate, Relevance gate, Forget gate, Output gate]**

&#10230; [Cổng cập nhật, Cổng relevance, Cổng quên, Cổng ra]

<br>


**34. [How much past should matter now?, Drop previous information?, Erase a cell or not?, How much to reveal of a cell?]**

&#10230; [Dữ liệu cũ nên có tầm quan trọng như thế nào ở hiện tại?, Bỏ qua thông tin phía trước?, Xoá ô hay không xoá?, Biểu thị một ô ở mức độ bao nhiêu?]

<br>


**35. [LSTM, GRU]**

&#10230; [LSTM, GRU]

<br>


**36. GRU/LSTM ― Gated Recurrent Unit (GRU) and Long Short-Term Memory units (LSTM) deal with the vanishing gradient problem encountered by traditional RNNs, with LSTM being a generalization of GRU. Below is a table summing up the characterizing equations of each architecture:**

&#10230; GRU/LSTM ― Gated Recurrent Unit (GRU) và Các đơn vị bộ nhớ dài-ngắn hạn (LSTM) đối phó với vấn đề vanishing gradient khi gặp phải bằng mạng RNNs truyền thống, với LSTM là sự tổng quát của GRU. Phía dưới là bảng tổng kết các phương trình đặc trưng của mỗi kiến trúc: 

<br>


**37. [Characterization, Gated Recurrent Unit (GRU), Long Short-Term Memory (LSTM), Dependencies]**

&#10230; [Đặc tính, Gated Recurrent Unit (GRU), Bộ nhớ dài-ngắn hạn (LSTM), Các phụ thuộc]

<br>


**38. Remark: the sign ⋆ denotes the element-wise multiplication between two vectors.**

&#10230; Chú ý: kí hiệu ⋆ chỉ phép nhân từng phần tử với nhau giữa hai vectors.

<br>


**39. Variants of RNNs ― The table below sums up the other commonly used RNN architectures:**

&#10230; Các biến thể của RNNs - Bảng dưới đây tổng kết các kiến trúc thường được sử dụng khác của RNN:

<br>


**40. [Bidirectional (BRNN), Deep (DRNN)]**

&#10230; [RNN hai chiều (Bidirectional - BRNN), RNN sâu (Deep - DRNN)]

<br>


**41. Learning word representation**

&#10230; Học từ đại diện

<br>


**42. In this section, we note V the vocabulary and |V| its size.**

&#10230; Trong phần này, chúng ta kí hiệu V là tập từ vựng và |V| là kích cỡ của nó.

<br>


**43. Motivation and notations**

&#10230; Giải thích và các kí hiệu

<br>


**44. Representation techniques ― The two main ways of representing words are summed up in the table below:**

&#10230; Các kĩ thuật biểu diễn - Có hai cách chính để biểu diễn từ được tổng kết ở bảng bên dưới:

<br>


**45. [1-hot representation, Word embedding]**

&#10230; [Biểu diễn 1-hot, Word embedding]

<br>


**46. [teddy bear, book, soft]**

&#10230; [gấu bông, sách, mềm]

<br>


**47. [Noted ow, Naive approach, no similarity information, Noted ew, Takes into account words similarity]**

&#10230; [Lưu ý ow, Tiếp cận Naive, không có thông tin chung, Lưu ý ew, Xem xét độ tương đồng của các từ]

<br>


**48. Embedding matrix ― For a given word w, the embedding matrix E is a matrix that maps its 1-hot representation ow to its embedding ew as follows:**

&#10230; Embedding matrix - Cho một từ w, embedding matrix E là một ma trận tham chiếu thể hiện 1-hot ow của nó với embedding ew của nó như sau:

<br>


**49. Remark: learning the embedding matrix can be done using target/context likelihood models.**

&#10230; Chú ý: học embedding matrix có thể hoàn thành bằng cách sử dụng các mô hình target/context likelihood.

<br>


**50. Word embeddings**

&#10230; Word embeddings

<br>


**51. Word2vec ― Word2vec is a framework aimed at learning word embeddings by estimating the likelihood that a given word is surrounded by other words. Popular models include skip-gram, negative sampling and CBOW.**

&#10230; Word2vec - Word2vec là một framework tập trung vào việc học word embeddings bằng cách ước lượng khả năng mà một từ cho trước được bao quanh bởi các từ khác. Các mô hình phổ biến bao gồm skip-gram, negative sampling và CBOW.

<br>


**52. [A cute teddy bear is reading, teddy bear, soft, Persian poetry, art]**

&#10230; [Một chú gấu bông dễ thương đang đọc sách, gấu bông teddy, soft, thơ Persian, hội hoạ]

<br>


**53. [Train network on proxy task, Extract high-level representation, Compute word embeddings]**

&#10230; [Huấn luyện mạng trên proxy task, Bóc tách các thể hiện cấp cao, Tính toán word embeddings]

<br>


**54. Skip-gram ― The skip-gram word2vec model is a supervised learning task that learns word embeddings by assessing the likelihood of any given target word t happening with a context word c. By noting θt a parameter associated with t, the probability P(t|c) is given by:**

&#10230; Skip-gram - Mô hình skip-gram word2vec là một task supervised learning, nó học các word embeddings bằng cách đánh giá khả năng của bất kì target word t cho trước nào xảy ra với context word c. Bằng việc kí hiệu θt là tham số đi kèm với t, xác suất P(t|c) được tính như sau:

<br>


**55. Remark: summing over the whole vocabulary in the denominator of the softmax part makes this model computationally expensive. CBOW is another word2vec model using the surrounding words to predict a given word.**

&#10230; Chú ý: Cộng tổng tất cả các từ vựng trong mẫu số của phần softmax khiến mô hình này tốn nhiều chi phí tính toán. CBOW là một mô hình word2vec khác sử dụng các từ xung quanh để dự đoán một từ cho trước.

<br>


**56. Negative sampling ― It is a set of binary classifiers using logistic regressions that aim at assessing how a given context and a given target words are likely to appear simultaneously, with the models being trained on sets of k negative examples and 1 positive example. Given a context word c and a target word t, the prediction is expressed by:**

&#10230; Negative sampling ― Nó là một tập của các bộ phân loại nhị phân sử dụng logistic regressions với mục tiêu là đánh giá khả năng mà một ngữ cảnh cho trước và các target words cho trước có thể xuất hiện đồng thời, với các mô hình đang được huấn luyện trên các tập của k negative examples và 1 positive example. Cho trước context word c và target word t, dự đoán được thể hiện bởi:

<br>


**57. Remark: this method is less computationally expensive than the skip-gram model.**

&#10230; Chú ý: phương thức này tốn ít chi phí tính toán hơn mô hình skip-gram.

<br>


**57bis. GloVe ― The GloVe model, short for global vectors for word representation, is a word embedding technique that uses a co-occurence matrix X where each Xi,j denotes the number of times that a target i occurred with a context j. Its cost function J is as follows:**

&#10230; GloVe - Mô hình GloVe, viết tắt của global vectors for word representation, nó là một kĩ thuật word embedding sử dụng ma trận đồng xuất hiện X với mỗi Xi,j là số lần mà từ đích (target) i xuất hiện tại ngữ cảnh j. Cost function J của nó như sau:

<br>


**58. where f is a weighting function such that Xi,j=0⟹f(Xi,j)=0.
Given the symmetry that e and θ play in this model, the final word embedding e(final)w is given by:**

&#10230; f là hàm trong số với Xi,j=0⟹f(Xi,j)=0. Với tính đối xứng mà e và θ có được trong mô hình này, word embedding cuối cùng e(final)w được định nghĩa như sau:

<br>


**59. Remark: the individual components of the learned word embeddings are not necessarily interpretable.**

&#10230; Chú ý: Các phần tử riêng của các word embedding học được không nhất thiết là phải thông dịch được.

<br>


**60. Comparing words**

&#10230; So sánh các từ

<br>


**61. Cosine similarity ― The cosine similarity between words w1 and w2 is expressed as follows:**

&#10230; Độ tương đồng Cosine - Độ tương đồng cosine giữa các từ w1 và w2 được trình bày như sau:

<br>


**62. Remark: θ is the angle between words w1 and w2.**

&#10230; Chú ý: θ là góc giữa các từ w1 và w2.

<br>


**63. t-SNE ― t-SNE (t-distributed Stochastic Neighbor Embedding) is a technique aimed at reducing high-dimensional embeddings into a lower dimensional space. In practice, it is commonly used to visualize word vectors in the 2D space.**

&#10230; t-SNE ― t-SNE (t-distributed Stochastic Neighbor Embedding) là một kĩ thuật nhằm giảm đi số chiều của không gian embedding. Trong thực tế, nó thường được sử dụng để trực quan hoá các word vectors trong không gian 2 chiều (2D).

<br>


**64. [literature, art, book, culture, poem, reading, knowledge, entertaining, loveable, childhood, kind, teddy bear, soft, hug, cute, adorable]**

&#10230; [văn học, nghệ thuật, sách, văn hoá, thơ, đọc, hiểu biết, giải trí, ngôn tình, thiếu nhi, loại, gấu teddy, mềm, ôm, dễ thương, đáng mến]

<br>


**65. Language model**

&#10230; Mô hình ngôn ngữ

<br>


**66. Overview ― A language model aims at estimating the probability of a sentence P(y).**

&#10230; Tổng quan - Một mô hình ngôn ngữ sẽ dự đoán xác suất của một câu P(y).

<br>


**67. n-gram model ― This model is a naive approach aiming at quantifying the probability that an expression appears in a corpus by counting its number of appearance in the training data.**

&#10230; Mô hình n-gram - Mô hình này là cách tiếp cận naive với mục đích định lượng xác suất mà một biểu hiện xuất hiện trong văn bản bằng cách đếm số lần xuất hiện của nó trong tập dữ liệu huấn luyện.

<br>


**68. Perplexity ― Language models are commonly assessed using the perplexity metric, also known as PP, which can be interpreted as the inverse probability of the dataset normalized by the number of words T. The perplexity is such that the lower, the better and is defined as follows:**

&#10230; Độ hỗn tạp - Các mô hình ngôn ngữ thường được đánh giá dựa theo độ đo hỗ tạp, cũng được biết đến là PP, có thể được hiểu như là nghịch đảo xác suất của tập dữ liệu được chuẩn hoá bởi số lượng các từ T. Độ hỗn tạp càng thấp thì càng tốt và được định nghĩa như sau:

<br>


**69. Remark: PP is commonly used in t-SNE.**

&#10230; Chú ý: PP thường được sử dụng trong t-SNE.

<br>


**70. Machine translation**

&#10230; Dịch máy

<br>


**71. Overview ― A machine translation model is similar to a language model except it has an encoder network placed before. For this reason, it is sometimes referred as a conditional language model. The goal is to find a sentence y such that:**

&#10230; Tổng quan - Một mô hình dịch máy tương tự với mô hình ngôn ngữ ngoại trừ nó có một mạng encoder được đặt phía trước. Vì lí do này, đôi khi nó còn được biết đến là mô hình ngôn ngữ có điều kiện. Mục tiêu là tìm một câu văn y như sau:

<br>


**72. Beam search ― It is a heuristic search algorithm used in machine translation and speech recognition to find the likeliest sentence y given an input x.**

&#10230; Tìm kiếm Beam - Nó là một giải thuật tìm kiếm heuristic được sử dụng trong dịch máy và ghi nhận tiếng nói để tìm câu văn y đúng nhất tương ứng với đầu vào x.

<br>


**73. [Step 1: Find top B likely words y<1>, Step 2: Compute conditional probabilities y<k>|x,y<1>,...,y<k−1>, Step 3: Keep top B combinations x,y<1>,...,y<k>, End process at a stop word]**

&#10230; [Bước 1: Tìm top B các từ y<1>, Bước 2: Tính xác suất có điều kiện y<k>|x,y<1>,...,y<k-1>, Bước 3: Giữ top B các tổ hợp x,y<1>,...,y<k>, Kết thúc quá trình xử lí bằng một từ dừng]

<br>


**74. Remark: if the beam width is set to 1, then this is equivalent to a naive greedy search.**

&#10230; Chú ý: nếu độ rộng của beam được thiết lập là 1, thì nó tương đương với tìm kiếm tham lam naive. 

<br>


**75. Beam width ― The beam width B is a parameter for beam search. Large values of B yield to better result but with slower performance and increased memory. Small values of B lead to worse results but is less computationally intensive. A standard value for B is around 10.**

&#10230; Độ rộng Beam - Độ rộng beam B là một tham số của giải thuật tìm kiếm beam. Các giá trị lớn của B tạo ra kết quả tốt hơn nhưng với hiệu năng thấp hơn và lượng bộ nhớ sử dụng sẽ tăng.

<br>


**76. Length normalization ― In order to improve numerical stability, beam search is usually applied on the following normalized objective, often called the normalized log-likelihood objective, defined as:**

&#10230; Chuẩn hoá độ dài - Đến cải thiện tính ổn định, beam search thường được áp dụng mục tiêu chuẩn hoá sau, thường được gọi là mục tiêu chuẩn hoá log-likelihood, được định nghĩa như sau:

<br>


**77. Remark: the parameter α can be seen as a softener, and its value is usually between 0.5 and 1.**

&#10230; Chú ý: tham số α có thể được xem như là softener, và giá trị của nó thường nằm trong đoạn 0.5 và 1.

<br>


**78. Error analysis ― When obtaining a predicted translation ˆy that is bad, one can wonder why we did not get a good translation y∗ by performing the following error analysis:**

&#10230; Phân tích lỗi - Khi có được một bản dịch tồi ˆy, chúng ta có thể tự hỏi rằng tại sao chúng ta không có được một kết quả dịch tốt y∗ bằng việc thực hiện việc phân tích lỗi như sau:

<br>


**79. [Case, Root cause, Remedies]**

&#10230; [Trường hợp, Nguyên nhân sâu xa, Biện pháp khắc phục]

<br>


**80. [Beam search faulty, RNN faulty, Increase beam width, Try different architecture, Regularize, Get more data]**

&#10230; [Lỗi Beam search, lỗi RNN, Tăng beam width, Thử kiến trúc khác, Chính quy, Lấy nhiều dữ liệu hơn]

<br>


**81. Bleu score ― The bilingual evaluation understudy (bleu) score quantifies how good a machine translation is by computing a similarity score based on n-gram precision. It is defined as follows:**

&#10230; Điểm Bleu - Bilingual evaluation understudy (bleu) score định lượng mức độ tốt của dịch máy bằng cách tính một độ tương đồng dựa trên dự đoán n-gram. Nó được định nghĩa như sau:

<br>


**82. where pn is the bleu score on n-gram only defined as follows:**

&#10230; với pn là bleu score chỉ trên n-gram được định nghĩa như sau:

<br>


**83. Remark: a brevity penalty may be applied to short predicted translations to prevent an artificially inflated bleu score.**

&#10230; Chú ý: một mức phạt ngắn có thể được áp dụng với các dự đoán dịch ngắn để tránh việc làm thổi phồng giá trị bleu score.

<br>


**84. Attention**

&#10230; Chú ý

<br>


**85. Attention model ― This model allows an RNN to pay attention to specific parts of the input that is considered as being important, which improves the performance of the resulting model in practice. By noting α<t,t′> the amount of attention that the output y<t> should pay to the activation a<t′> and c<t> the context at time t, we have:**

&#10230; Attention model - Mô hình này cho phép một RNN tập trung vào các phần cụ thể của đầu vào được xem xét là quan trọng, nó giúp cải thiện hiệu năng của mô hình kết quả trong thực tế. Bằng việc kí hiệu α<t,t′> là mức độ chú ý mà đầu ra y<t> nên có đối với hàm kích hoạt a<t′> và c<t> là ngữ cảnh ở thời điểm t, chúng ta có:

<br>


**86. with**

&#10230; với

<br>


**87. Remark: the attention scores are commonly used in image captioning and machine translation.**

&#10230; Chú ý: Các attention scores thường được sử dụng trong chú thích ảnh và dịch máy.

<br>


**88. A cute teddy bear is reading Persian literature.**

&#10230; Một chú gấu bông dễ thương đang đọc bài văn Persian.

<br>


**89. Attention weight ― The amount of attention that the output y<t> should pay to the activation a<t′> is given by α<t,t′> computed as follows:**

&#10230; Attention weight - Sự chú ý mà đầu ra y<t> nên có với hàm kích hoạt a<t′> với α<t,t′> được tính như sau:

<br>


**90. Remark: computation complexity is quadratic with respect to Tx.**

&#10230; Chú ý: độ phức tạp tính toán là một phương trình bậc hai đối với Tx.

<br>


**91. The Deep Learning cheatsheets are now available in [target language].**

&#10230; Deep Learning cheatsheets hiện đã có bản dịch [tiếng việt].

<br>

**92. Original authors**

&#10230; Tác giả

<br>

**93. Translated by X, Y and Z**

&#10230; Dịch bởi X, Y và Z

<br>

**94. Reviewed by X, Y and Z**

&#10230; Reviewed bởi X, Y và Z

<br>

**95. View PDF version on GitHub**

&#10230; Xem bản PDF trên GibHub

<br>

**96. By X and Y**

&#10230; Bởi X và Y

<br>
