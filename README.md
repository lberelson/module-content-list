# module-content-list
conditional loop on matrix fields in EE to check for whether blank window is checked or not

{if row_count == "1"}
  <div  class="modFlex module">
  <h2 style="margin-bottom:6px;">{header}</h2>
  <ul>
  {/if}
  {if link_url} 
  <li><a href="{link_url}" target="{if link_target == "Yes"}_blank {if:else} target ="_self " "{/if}>{link_text} </a></li>

  {if:else}
  <li><a href="{link_asset}" target="{if link_target == "Yes"}_blank {if:else} target ="_self "  "{/if}> {link_text} </a></li>

  {/if}

  {if row_count == "{total_rows}"}</ul>
  </div><!--// end modFlex //-->
{/if}
