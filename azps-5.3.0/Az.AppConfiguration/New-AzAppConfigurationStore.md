---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423056"
---
# <span data-ttu-id="9bb36-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="9bb36-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="9bb36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9bb36-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb36-103">Skapar ett konfigurations Arkiv med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="9bb36-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="9bb36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9bb36-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9bb36-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9bb36-105">DESCRIPTION</span></span>
<span data-ttu-id="9bb36-106">Skapar ett konfigurations Arkiv med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="9bb36-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="9bb36-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9bb36-107">EXAMPLES</span></span>

### <span data-ttu-id="9bb36-108">Exempel 1: skapa ett program konfigurations Arkiv</span><span class="sxs-lookup"><span data-stu-id="9bb36-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="9bb36-109">Det här kommandot skapar en app-konfigurationsfil.</span><span class="sxs-lookup"><span data-stu-id="9bb36-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="9bb36-110">Exempel 2: skapa en app-konfiguration med IdentityType inställd på "UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="9bb36-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="9bb36-111">Det här kommandot skapar en program konfiguration och tilldelar en användardefinierad hanterad identitet till den.</span><span class="sxs-lookup"><span data-stu-id="9bb36-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="9bb36-112">I det här avsnittet finns information om hur `Update-AzAppConfigurationStore` du aktiverar CMK (cusomer-hanterad nycklar).</span><span class="sxs-lookup"><span data-stu-id="9bb36-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="9bb36-113">Exempel 3: skapa en app-konfiguration med IdentityType inställd på "SystemAssigned"</span><span class="sxs-lookup"><span data-stu-id="9bb36-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="9bb36-114">Det här kommandot skapar en program konfiguration och aktiverar den systemtilldelade hanterade identitet som är associerad med resursen.</span><span class="sxs-lookup"><span data-stu-id="9bb36-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="9bb36-115">I det här avsnittet finns information om hur `Update-AzAppConfigurationStore` du aktiverar CMK (cusomer-hanterad nycklar).</span><span class="sxs-lookup"><span data-stu-id="9bb36-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="9bb36-116">Exempel 4: skapa en app-konfiguration med IdentityType angivet till "SystemAssigned, UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="9bb36-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="9bb36-117">Du kan aktivera systemtilldelad hanterad identitet och ge användare som har tilldelade identiteter samtidigt.</span><span class="sxs-lookup"><span data-stu-id="9bb36-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="9bb36-118">I det här avsnittet finns information om hur `Update-AzAppConfigurationStore` du aktiverar CMK (cusomer-hanterad nycklar).</span><span class="sxs-lookup"><span data-stu-id="9bb36-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="9bb36-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9bb36-119">PARAMETERS</span></span>

### <span data-ttu-id="9bb36-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bb36-120">-AsJob</span></span>
<span data-ttu-id="9bb36-121">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="9bb36-121">Run the command as a job</span></span>

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

### <span data-ttu-id="9bb36-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb36-122">-DefaultProfile</span></span>
<span data-ttu-id="9bb36-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb36-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bb36-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9bb36-124">-IdentityType</span></span>
<span data-ttu-id="9bb36-125">Typ av hanterad identitet som används.</span><span class="sxs-lookup"><span data-stu-id="9bb36-125">The type of managed identity used.</span></span>
<span data-ttu-id="9bb36-126">Typen "SystemAssignedAndUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="9bb36-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="9bb36-127">Typen "inget" tar bort alla identiteter.</span><span class="sxs-lookup"><span data-stu-id="9bb36-127">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb36-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="9bb36-128">-Location</span></span>
<span data-ttu-id="9bb36-129">Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="9bb36-129">The location of the resource.</span></span>
<span data-ttu-id="9bb36-130">Det här kan inte ändras efter att resursen har skapats.</span><span class="sxs-lookup"><span data-stu-id="9bb36-130">This cannot be changed after the resource is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb36-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="9bb36-131">-Name</span></span>
<span data-ttu-id="9bb36-132">Konfigurations lagrets namn.</span><span class="sxs-lookup"><span data-stu-id="9bb36-132">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb36-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9bb36-133">-NoWait</span></span>
<span data-ttu-id="9bb36-134">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="9bb36-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9bb36-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bb36-135">-ResourceGroupName</span></span>
<span data-ttu-id="9bb36-136">Namnet på resurs gruppen som behållar registret tillhör.</span><span class="sxs-lookup"><span data-stu-id="9bb36-136">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb36-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="9bb36-137">-Sku</span></span>
<span data-ttu-id="9bb36-138">SKU-namnet på konfigurations butiken.</span><span class="sxs-lookup"><span data-stu-id="9bb36-138">The SKU name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb36-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9bb36-139">-SubscriptionId</span></span>
<span data-ttu-id="9bb36-140">Microsoft Azure-prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="9bb36-140">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb36-141">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9bb36-141">-Tag</span></span>
<span data-ttu-id="9bb36-142">Taggarna för resursen.</span><span class="sxs-lookup"><span data-stu-id="9bb36-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="9bb36-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9bb36-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="9bb36-144">Listan över användardefinierade identiteter associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="9bb36-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="9bb36-145">De användardefinierade nycklarna för identitets ord listor är ARM-resursposter i formatet: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="9bb36-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb36-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9bb36-146">-Confirm</span></span>
<span data-ttu-id="9bb36-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9bb36-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bb36-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bb36-148">-WhatIf</span></span>
<span data-ttu-id="9bb36-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9bb36-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bb36-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9bb36-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bb36-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb36-151">CommonParameters</span></span>
<span data-ttu-id="9bb36-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bb36-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb36-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bb36-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb36-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9bb36-154">INPUTS</span></span>

## <span data-ttu-id="9bb36-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9bb36-155">OUTPUTS</span></span>

### <span data-ttu-id="9bb36-156">Microsoft. Azure. PowerShell. cmdletar. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="9bb36-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="9bb36-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9bb36-157">NOTES</span></span>

<span data-ttu-id="9bb36-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9bb36-158">ALIASES</span></span>

## <span data-ttu-id="9bb36-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9bb36-159">RELATED LINKS</span></span>



[<span data-ttu-id="9bb36-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9bb36-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

