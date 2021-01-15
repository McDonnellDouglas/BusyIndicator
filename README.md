# BusyIndicator
BusyIndicator for WPF with multiple indicator types  

<img src="https://github.com/Peoky/BusyIndicator/blob/main/Images/DashLoader.gif" alt="Dash Loader" width="45%"></img>
<img src="https://github.com/Peoky/BusyIndicator/blob/main/Images/DotLoader.gif" alt="Dot Loader" width="45%"></img>
<img src="https://github.com/Peoky/BusyIndicator/blob/main/Images/ProgressBar.gif" alt="Progress Bar" width="45%"></img>
<img src="https://github.com/Peoky/BusyIndicator/blob/main/Images/ProgressRing.gif" alt="Progress Ring" width="45%"></img>
<img src="https://github.com/Peoky/BusyIndicator/blob/main/Images/Spinner.gif" alt="Spinner" width="45%"></img>  

## Prerequisites:
<ul><li>.Net Framework 4.7.2 or higher</li></ul>  

## How to use:
1. Install the package via NuGet    
<pre>Install-Package BusyIndicator</pre>  

2. Add resources to App.xaml  
<pre><code>&lt;ResourceDictionary&gt;
            &lt;ResourceDictionary.MergedDictionaries&gt;
                &lt;ResourceDictionary&gt;
                    &lt;ResourceDictionary.MergedDictionaries&gt;
                        &lt;ResourceDictionary Source="pack://application:,,,/BusyIndicator;component/BusyMask/BusyMask.xaml"/&gt;
                        &lt;ResourceDictionary Source="pack://application:,,,/BusyIndicator;component/Indicator/Indicator.xaml"/&gt;
                    &lt;/ResourceDictionary.MergedDictionaries&gt;
                &lt;/ResourceDictionary&gt;
            &lt;/ResourceDictionary.MergedDictionaries&gt;
&lt;/ResourceDictionary&gt;
</code></pre>  

3. Add a reference to the library in your view  
<pre>xmlns:busyindicator="clr-namespace:BusyIndicator;assembly=BusyIndicator"</pre>  

4. Create a BusyMask on top of your view  
<pre><code>&lt;busyindicator:BusyMask x:Name="BusyIndicator" IsBusy="False" IndicatorType="DashLoader" BusyContent="Please wait..." &gt; `your view code goes here` &lt;/busyindicator:BusyMask&gt;</code></pre>  

5. Set `IsBusy` property value to `true` or `false` to enable or disable the mask (or bind it)
<pre>BusyIndicator.IsBusy = true; or BusyIndicator.IsBusy = false; </pre>



