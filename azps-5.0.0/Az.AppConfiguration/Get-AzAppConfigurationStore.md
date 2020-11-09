---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326022"
---
# <span data-ttu-id="70f3b-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="70f3b-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="70f3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="70f3b-103">Hämta eller lista program konfigurations arkiv.</span><span class="sxs-lookup"><span data-stu-id="70f3b-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="70f3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70f3b-104">SYNTAX</span></span>

### <span data-ttu-id="70f3b-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="70f3b-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="70f3b-106">Lära</span><span class="sxs-lookup"><span data-stu-id="70f3b-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="70f3b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="70f3b-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="70f3b-108">List1</span><span class="sxs-lookup"><span data-stu-id="70f3b-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="70f3b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70f3b-109">DESCRIPTION</span></span>
<span data-ttu-id="70f3b-110">Hämta eller lista program konfigurations arkiv.</span><span class="sxs-lookup"><span data-stu-id="70f3b-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="70f3b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70f3b-111">EXAMPLES</span></span>

### <span data-ttu-id="70f3b-112">Exempel 1: lista alla program konfigurations Arkiv under ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="70f3b-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="70f3b-113">Det här kommandot visar alla program konfigurations Arkiv under ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="70f3b-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="70f3b-114">Exempel 2: lista alla program konfigurations Arkiv under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="70f3b-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="70f3b-115">Det här kommandot visar alla program konfigurations Arkiv under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="70f3b-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="70f3b-116">Exempel 3: Hämta ett app-konfigurationsinställningar efter namn</span><span class="sxs-lookup"><span data-stu-id="70f3b-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="70f3b-117">Det här kommandot får en app-konfigurationsfil efter namn.</span><span class="sxs-lookup"><span data-stu-id="70f3b-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="70f3b-118">Exempel 4: Hämta ett app-konfigurationsinställningar via pipeline</span><span class="sxs-lookup"><span data-stu-id="70f3b-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="70f3b-119">Det här kommandot får en app-konfigurationsfil via pipeline.</span><span class="sxs-lookup"><span data-stu-id="70f3b-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="70f3b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70f3b-120">PARAMETERS</span></span>

### <span data-ttu-id="70f3b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f3b-121">-DefaultProfile</span></span>
<span data-ttu-id="70f3b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70f3b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70f3b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70f3b-123">-InputObject</span></span>
<span data-ttu-id="70f3b-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="70f3b-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70f3b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="70f3b-125">-Name</span></span>
<span data-ttu-id="70f3b-126">Konfigurations lagrets namn.</span><span class="sxs-lookup"><span data-stu-id="70f3b-126">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f3b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70f3b-127">-ResourceGroupName</span></span>
<span data-ttu-id="70f3b-128">Namnet på resurs gruppen som behållar registret tillhör.</span><span class="sxs-lookup"><span data-stu-id="70f3b-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f3b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70f3b-129">-SubscriptionId</span></span>
<span data-ttu-id="70f3b-130">Microsoft Azure-prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="70f3b-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f3b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f3b-131">CommonParameters</span></span>
<span data-ttu-id="70f3b-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70f3b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f3b-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70f3b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f3b-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70f3b-134">INPUTS</span></span>

### <span data-ttu-id="70f3b-135">Microsoft. Azure. PowerShell. cmdletar. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="70f3b-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="70f3b-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70f3b-136">OUTPUTS</span></span>

### <span data-ttu-id="70f3b-137">Microsoft. Azure. PowerShell. cmdletar. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="70f3b-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="70f3b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70f3b-138">NOTES</span></span>

<span data-ttu-id="70f3b-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="70f3b-139">ALIASES</span></span>

<span data-ttu-id="70f3b-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="70f3b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="70f3b-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="70f3b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="70f3b-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="70f3b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="70f3b-143">INPUTOBJECT <IAppConfigurationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="70f3b-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="70f3b-144">`[ConfigStoreName <String>]`: Konfigurations lagrets namn.</span><span class="sxs-lookup"><span data-stu-id="70f3b-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="70f3b-145">`[GroupName <String>]`: Namnet på den privata länk resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="70f3b-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="70f3b-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="70f3b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="70f3b-147">`[PrivateEndpointConnectionName <String>]`: Namn på privat slut punkt</span><span class="sxs-lookup"><span data-stu-id="70f3b-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="70f3b-148">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som behållar registret tillhör.</span><span class="sxs-lookup"><span data-stu-id="70f3b-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="70f3b-149">`[SubscriptionId <String>]`: ID för Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="70f3b-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="70f3b-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70f3b-150">RELATED LINKS</span></span>

