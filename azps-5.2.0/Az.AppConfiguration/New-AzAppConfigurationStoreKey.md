---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98387828"
---
# <span data-ttu-id="f4466-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="f4466-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="f4466-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4466-102">SYNOPSIS</span></span>
<span data-ttu-id="f4466-103">Återskapar en åtkomst-nyckeln för det angivna konfigurations arkivet.</span><span class="sxs-lookup"><span data-stu-id="f4466-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="f4466-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4466-104">SYNTAX</span></span>

### <span data-ttu-id="f4466-105">RegenerateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="f4466-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f4466-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f4466-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f4466-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4466-107">DESCRIPTION</span></span>
<span data-ttu-id="f4466-108">Återskapar en åtkomst-nyckeln för det angivna konfigurations arkivet.</span><span class="sxs-lookup"><span data-stu-id="f4466-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="f4466-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4466-109">EXAMPLES</span></span>

### <span data-ttu-id="f4466-110">Exempel 1: återskapa nyckeln för ett program konfigurations Arkiv</span><span class="sxs-lookup"><span data-stu-id="f4466-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="f4466-111">Det här kommandot återskapar en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="f4466-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="f4466-112">Exempel 2: återskapa nyckeln för ett program konfigurations Arkiv per objekt</span><span class="sxs-lookup"><span data-stu-id="f4466-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="f4466-113">Det här kommandot återskapar en lagrings plats för en app-konfiguration per objekt.</span><span class="sxs-lookup"><span data-stu-id="f4466-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="f4466-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4466-114">PARAMETERS</span></span>

### <span data-ttu-id="f4466-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4466-115">-DefaultProfile</span></span>
<span data-ttu-id="f4466-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4466-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4466-117">-ID</span><span class="sxs-lookup"><span data-stu-id="f4466-117">-Id</span></span>
<span data-ttu-id="f4466-118">ID för nyckeln som ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="f4466-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="f4466-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4466-119">-InputObject</span></span>
<span data-ttu-id="f4466-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f4466-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4466-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4466-121">-Name</span></span>
<span data-ttu-id="f4466-122">Konfigurations lagrets namn.</span><span class="sxs-lookup"><span data-stu-id="f4466-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4466-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4466-123">-ResourceGroupName</span></span>
<span data-ttu-id="f4466-124">Namnet på resurs gruppen som behållar registret tillhör.</span><span class="sxs-lookup"><span data-stu-id="f4466-124">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4466-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4466-125">-SubscriptionId</span></span>
<span data-ttu-id="f4466-126">Microsoft Azure-prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="f4466-126">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4466-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4466-127">-Confirm</span></span>
<span data-ttu-id="f4466-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4466-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4466-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4466-129">-WhatIf</span></span>
<span data-ttu-id="f4466-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4466-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4466-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4466-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4466-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4466-132">CommonParameters</span></span>
<span data-ttu-id="f4466-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4466-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4466-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4466-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4466-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4466-135">INPUTS</span></span>

### <span data-ttu-id="f4466-136">Microsoft. Azure. PowerShell. cmdletar. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="f4466-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="f4466-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4466-137">OUTPUTS</span></span>

### <span data-ttu-id="f4466-138">Microsoft. Azure. PowerShell. cmdletar. AppConfiguration. Models. Api20200601. IApiKey</span><span class="sxs-lookup"><span data-stu-id="f4466-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="f4466-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4466-139">NOTES</span></span>

<span data-ttu-id="f4466-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f4466-140">ALIASES</span></span>

<span data-ttu-id="f4466-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="f4466-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4466-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="f4466-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4466-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4466-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4466-144">INPUTOBJECT <IAppConfigurationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="f4466-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4466-145">`[ConfigStoreName <String>]`: Konfigurations lagrets namn.</span><span class="sxs-lookup"><span data-stu-id="f4466-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="f4466-146">`[GroupName <String>]`: Namnet på den privata länk resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f4466-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="f4466-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f4466-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4466-148">`[PrivateEndpointConnectionName <String>]`: Namn på privat slut punkt</span><span class="sxs-lookup"><span data-stu-id="f4466-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="f4466-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som behållar registret tillhör.</span><span class="sxs-lookup"><span data-stu-id="f4466-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="f4466-150">`[SubscriptionId <String>]`: ID för Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f4466-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="f4466-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4466-151">RELATED LINKS</span></span>

