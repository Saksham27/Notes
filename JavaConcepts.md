---


---

<h1 id="access-modifiers-">Access Modifiers :</h1>
<h3 id="public">public</h3>
<p>public Members (variables, methods, and constructors) declared public within a public class are visible to any class in the Java program, whether these classes are in the same package or in another package.</p>
<h3 id="protected">protected</h3>
<p>The protected fields or methods, cannot be used for classes and Interfaces. Fields, methods and constructors declared protected in a super-class can be accessed only by sub-classes in other packages. Classes in the same package can also access protected fields, methods and constructors as well, even if they are not a subclass of the protected member’s class.</p>
<h3 id="default-no-value">Default (no value)</h3>
<p>The default access level is declared by not writing any access modifier at all. Any class, field, method or constructor that has no declared access modifier is accessible only by classes in the same package.</p>
<h3 id="private">private</h3>
<p>The private (most restrictive) modifiers can be used for members but cannot be used for classes and Interfaces. Fields, methods or constructors declared private are strictly controlled, which means they cannot be accessed by anywhere outside the enclosing class.</p>
<h1 id="modifiers-">Modifiers :</h1>
<h3 id="static">static</h3>
<p>static can be used for members of a class. The static members of the class can be accessed without creating an object of a class.</p>
<h3 id="final">final</h3>
<p>This modifier applicable to class, method, and variables. This modifier tells the compiler not to change the value of a variable once assigned. If applied to class, it cannot be sub-classed. If applied to a method, the method cannot be overridden in sub-class.</p>
<h3 id="abstract">abstract</h3>
<p>There are situations in which you will want to define a super-class that declares the structure of a given abstraction without providing a complete implementation of every method. This modifier is applicable to class and methods only.</p>

<table>
<thead>
<tr>
<th>Modifier</th>
<th>class</th>
<th>constructor</th>
<th>method</th>
<th>Data/variables</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>public</em></td>
<td>yes</td>
<td>yes</td>
<td>yes</td>
<td>yes</td>
</tr>
<tr>
<td><em>protected</em></td>
<td></td>
<td>yes</td>
<td>yes</td>
<td>yes</td>
</tr>
<tr>
<td><em>default</em></td>
<td>yes</td>
<td>yes</td>
<td>yes</td>
<td>yes</td>
</tr>
<tr>
<td><em>final</em></td>
<td></td>
<td>yes</td>
<td>yes</td>
<td>yes</td>
</tr>
<tr>
<td><em>static</em></td>
<td></td>
<td></td>
<td>yes</td>
<td></td>
</tr>
<tr>
<td><em>final</em></td>
<td>yes</td>
<td></td>
<td>yes</td>
<td></td>
</tr>
</tbody>
</table><h1 id="packages-">Packages :</h1>
<pre class=" language-java"><code class="prism  language-java"><span class="token keyword">package</span> com<span class="token punctuation">.</span>sct<span class="token punctuation">.</span>calculate<span class="token punctuation">;</span>
<span class="token keyword">public</span>  <span class="token keyword">class</span>  <span class="token class-name">MyCalculation</span>  <span class="token punctuation">{</span>
	<span class="token comment">//This method calculate interst</span>
	<span class="token keyword">public</span>  <span class="token keyword">int</span>  <span class="token function">calculateInterest</span><span class="token punctuation">(</span><span class="token keyword">int</span> amount<span class="token punctuation">,</span>  <span class="token keyword">int</span> rate<span class="token punctuation">)</span>  <span class="token punctuation">{</span>
	<span class="token keyword">int</span> intrerstAmount <span class="token operator">=</span> amount <span class="token operator">*</span> rate<span class="token operator">/</span><span class="token number">100</span><span class="token punctuation">;</span>  
	<span class="token keyword">return</span> intrerstAmount<span class="token punctuation">;</span>  
	<span class="token punctuation">}</span>  
<span class="token punctuation">}</span>
</code></pre>
<ol>
<li>Calling with fully qualified name.  <code>// line no 6 below</code></li>
<li>package import and then directly calling the method <code>// line no 7 below</code></li>
</ol>
<pre class=" language-java"><code class="prism  language-java"> <span class="token keyword">package</span> com<span class="token punctuation">.</span>sct<span class="token punctuation">.</span>account<span class="token punctuation">;</span>
 <span class="token keyword">import</span> com<span class="token punctuation">.</span>sct<span class="token punctuation">.</span>calculate<span class="token punctuation">.</span>*<span class="token punctuation">;</span>
 <span class="token keyword">public</span>  <span class="token keyword">class</span>  <span class="token class-name">SalesTax</span>  <span class="token punctuation">{</span>
   <span class="token keyword">public</span>  <span class="token keyword">static</span>  <span class="token keyword">void</span>  <span class="token function">main</span>  <span class="token punctuation">(</span>String args<span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">int</span> interestAmount <span class="token operator">=</span>  <span class="token keyword">new</span> <span class="token class-name">com<span class="token punctuation">.</span>sct<span class="token punctuation">.</span>calculate<span class="token punctuation">.</span>MyCalculation</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">calculateInterest</span><span class="token punctuation">(</span><span class="token number">1000</span><span class="token punctuation">,</span>  <span class="token number">8</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// line 6</span>
      System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Interest Amount = "</span><span class="token operator">+</span> interestAmount<span class="token punctuation">)</span><span class="token punctuation">;</span>
      <span class="token keyword">int</span> intAmount2 <span class="token operator">=</span>  <span class="token keyword">new</span>  <span class="token class-name">MyCalculation</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">calculateInterest</span><span class="token punctuation">(</span><span class="token number">1000</span><span class="token punctuation">,</span><span class="token number">8</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// line 7</span>
      System<span class="token punctuation">.</span>out<span class="token punctuation">.</span><span class="token function">println</span><span class="token punctuation">(</span><span class="token string">"Interest Amount2= "</span><span class="token operator">+</span> intAmount2<span class="token punctuation">)</span><span class="token punctuation">;</span>
      <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h1 id="object-oriented-programming---oops--">Object Oriented Programming  ( OOP’s ) :</h1>
<ul>
<li>A class is a blueprint with some properties/behaviours and methods.</li>
<li>An object is an instance of a Class.</li>
<li>Three main features of OOP’s -
<ol>
<li><strong>Encapsulation</strong></li>
<li><strong>Inheritance</strong></li>
<li><strong>Polymorphism</strong></li>
</ol>
</li>
</ul>
<h3 id="encapsulation-">Encapsulation :</h3>
<p>Encapsulation means putting together all the variables (instance variables) and the methods into a single unit called Class. It also means hiding data and methods within an Object. Encapsulation provides the security that keeps data and methods safe from inadvertent changes. Programmers sometimes refer to encapsulation as using a “black box,” or a device that you can use without regard to the internal mechanisms. A programmer can access and use the methods and data contained in the black box but cannot change them.</p>
<pre class=" language-java"><code class="prism  language-java"><span class="token keyword">package</span> oopsconcept<span class="token punctuation">;</span>
<span class="token keyword">public</span> <span class="token keyword">class</span> <span class="token class-name">Mobile</span> <span class="token punctuation">{</span>	
	<span class="token keyword">private</span> String manufacturer<span class="token punctuation">;</span>
	<span class="token keyword">private</span> String operating_system<span class="token punctuation">;</span>
	<span class="token keyword">public</span> String model<span class="token punctuation">;</span>
	<span class="token keyword">private</span> <span class="token keyword">int</span> cost<span class="token punctuation">;</span>
	<span class="token comment">//Constructor to set properties/characteristics of object</span>
	<span class="token function">Mobile</span><span class="token punctuation">(</span>String man<span class="token punctuation">,</span> String o<span class="token punctuation">,</span>String m<span class="token punctuation">,</span> <span class="token keyword">int</span> c<span class="token punctuation">)</span><span class="token punctuation">{</span>
		<span class="token keyword">this</span><span class="token punctuation">.</span>manufacturer <span class="token operator">=</span> man<span class="token punctuation">;</span>
		<span class="token keyword">this</span><span class="token punctuation">.</span>operating_system<span class="token operator">=</span>o<span class="token punctuation">;</span>
		<span class="token keyword">this</span><span class="token punctuation">.</span>model<span class="token operator">=</span>m<span class="token punctuation">;</span>
		<span class="token keyword">this</span><span class="token punctuation">.</span>cost<span class="token operator">=</span>c<span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
	<span class="token comment">//Method to get access Model property of Object</span>
	<span class="token keyword">public</span> String <span class="token function">getModel</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">{</span>
		<span class="token keyword">return</span> <span class="token keyword">this</span><span class="token punctuation">.</span>model<span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
	<span class="token comment">// We can add other method to get access to other properties</span>
<span class="token punctuation">}</span>
</code></pre>

