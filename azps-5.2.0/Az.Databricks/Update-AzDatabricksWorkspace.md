---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414195"
---
# <span data-ttu-id="f7c2a-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="f7c2a-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="f7c2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c2a-103">Uppdaterar en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-103">Updates a workspace.</span></span>

## <span data-ttu-id="f7c2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7c2a-104">SYNTAX</span></span>

### <span data-ttu-id="f7c2a-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="f7c2a-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f7c2a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f7c2a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f7c2a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7c2a-107">DESCRIPTION</span></span>
<span data-ttu-id="f7c2a-108">Uppdaterar en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-108">Updates a workspace.</span></span>

## <span data-ttu-id="f7c2a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7c2a-109">EXAMPLES</span></span>

### <span data-ttu-id="f7c2a-110">Exempel 1: uppdaterar taggarna för en Databricks-arbetsyta</span><span class="sxs-lookup"><span data-stu-id="f7c2a-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="f7c2a-111">Det här kommandot uppdaterar taggarna för en Databricks-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="f7c2a-112">Exempel 2: Aktivera kryptering på en Databricks-arbetsyta</span><span class="sxs-lookup"><span data-stu-id="f7c2a-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="f7c2a-113">Det tar tre steg att aktivera kryptering på en Databricks-arbets yta:</span><span class="sxs-lookup"><span data-stu-id="f7c2a-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="f7c2a-114">Uppdatera arbets ytan med `-PrepareEncryption` (om den inte skapades).</span><span class="sxs-lookup"><span data-stu-id="f7c2a-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="f7c2a-115">Hitta `StorageAccountIdentityPrincipalId` i resultatet av det sista steget.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="f7c2a-116">Bevilja viktiga behörigheter för huvud kontot.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="f7c2a-117">Uppdatera arbets ytan igen för att fylla i information om krypterings knappen:</span><span class="sxs-lookup"><span data-stu-id="f7c2a-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="f7c2a-118">Exempel 3: inaktivera kryptering på en Databricks-arbetsyta</span><span class="sxs-lookup"><span data-stu-id="f7c2a-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="f7c2a-119">Om du vill inaktivera krypteringen ställer du in den `-EncryptionKeySource` `'Default'` .</span><span class="sxs-lookup"><span data-stu-id="f7c2a-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="f7c2a-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7c2a-120">PARAMETERS</span></span>

### <span data-ttu-id="f7c2a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7c2a-121">-AsJob</span></span>
<span data-ttu-id="f7c2a-122">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="f7c2a-122">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c2a-123">-DefaultProfile</span></span>
<span data-ttu-id="f7c2a-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="f7c2a-125">-EncryptionKeyName</span></span>
<span data-ttu-id="f7c2a-126">Namnet på Key valv-tangenten.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-126">The name of Key Vault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="f7c2a-127">-EncryptionKeySource</span></span>
<span data-ttu-id="f7c2a-128">Krypterings-källa (leverantör).</span><span class="sxs-lookup"><span data-stu-id="f7c2a-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="f7c2a-129">Möjliga värden (Skift läges okänsligt): standard, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Support.KeySource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="f7c2a-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="f7c2a-131">Key-valvets URI (DNS-namn).</span><span class="sxs-lookup"><span data-stu-id="f7c2a-131">The URI (DNS name) of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f7c2a-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="f7c2a-133">Versionen av Key valv-tangenten.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-133">The version of KeyVault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7c2a-134">-InputObject</span></span>
<span data-ttu-id="f7c2a-135">Identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-135">Identity parameter.</span></span>
<span data-ttu-id="f7c2a-136">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7c2a-137">-Name</span></span>
<span data-ttu-id="f7c2a-138">Namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-138">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-139">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f7c2a-139">-NoWait</span></span>
<span data-ttu-id="f7c2a-140">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="f7c2a-140">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="f7c2a-141">-PrepareEncryption</span></span>
<span data-ttu-id="f7c2a-142">Förbereda arbets ytan för kryptering.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="f7c2a-143">Aktiverar hanterad identitet för hanterat lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-143">Enables the Managed Identity for managed storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c2a-144">-ResourceGroupName</span></span>
<span data-ttu-id="f7c2a-145">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-145">The name of the resource group.</span></span>
<span data-ttu-id="f7c2a-146">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-146">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7c2a-147">-SubscriptionId</span></span>
<span data-ttu-id="f7c2a-148">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-148">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-149">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f7c2a-149">-Tag</span></span>
<span data-ttu-id="f7c2a-150">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f7c2a-151">-Confirm</span></span>
<span data-ttu-id="f7c2a-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7c2a-153">-WhatIf</span></span>
<span data-ttu-id="f7c2a-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7c2a-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c2a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c2a-156">CommonParameters</span></span>
<span data-ttu-id="f7c2a-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c2a-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7c2a-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c2a-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7c2a-159">INPUTS</span></span>

### <span data-ttu-id="f7c2a-160">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="f7c2a-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="f7c2a-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7c2a-161">OUTPUTS</span></span>

### <span data-ttu-id="f7c2a-162">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="f7c2a-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="f7c2a-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7c2a-163">NOTES</span></span>

<span data-ttu-id="f7c2a-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f7c2a-164">ALIASES</span></span>

<span data-ttu-id="f7c2a-165">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="f7c2a-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f7c2a-166">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f7c2a-167">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f7c2a-168">INPUTOBJECT <IDatabricksIdentity> : identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="f7c2a-169">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f7c2a-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f7c2a-170">`[PeeringName <String>]`: Namnet på arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="f7c2a-171">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f7c2a-172">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="f7c2a-173">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f7c2a-174">`[WorkspaceName <String>]`: Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="f7c2a-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="f7c2a-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7c2a-175">RELATED LINKS</span></span>

