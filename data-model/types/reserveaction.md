---
description: This page describes the ReserveAction type.
---

# ReserveAction

This type is derived from [https://schema.org/ReserveAction](https://schema.org/ReserveAction).

## **Fields**

### **Optional fields**
    
<table>
  <thead>
    <tr>
      <th style="text-align:left">Property</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>type</b></td>
      <td style="text-align:left">
        <a href="https://schema.org/Text"><code>Text</code></a>
      </td>
      <td style="text-align:left">
        Must always be present and set to <code>ReserveAction</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>name</b></td>
      <td style="text-align:left">
        <a href="https://schema.org/Text"><code>Text</code></a>
      </td>
      <td style="text-align:left">
        The name of the action</br></br><b>Example</b></br></br><code>Book</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>target</b></td>
      <td style="text-align:left">
        <a href="https://docs.openactive.io/data-model/types/entrypoint"><code>EntryPoint</code></a>
      </td>
      <td style="text-align:left">
        A definition of the target of the action.</br></br><b>Example</b></br></br><code>{<br/>&nbsp;&nbsp;&quot;encodingType&quot;:&nbsp;&quot;application/vnd.openactive.v1.0+json&quot;,<br/>&nbsp;&nbsp;&quot;httpMethod&quot;:&nbsp;&quot;POST&quot;,<br/>&nbsp;&nbsp;&quot;type&quot;:&nbsp;&quot;EntryPoint&quot;,<br/>&nbsp;&nbsp;&quot;url&quot;:&nbsp;&quot;https://example.com/orders&quot;<br/>}</code>
      </td>
    </tr>
  </tbody>
</table>

