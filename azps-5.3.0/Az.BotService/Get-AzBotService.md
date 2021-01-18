---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 4324c1e78ce56cc4b56455eaaff266b52c1d87d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524645"
---
# <span data-ttu-id="1c763-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="1c763-101">Get-AzBotService</span></span>

## <span data-ttu-id="1c763-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c763-102">SYNOPSIS</span></span>
<span data-ttu-id="1c763-103">Returnerar en BotService som anges av parametrarna.</span><span class="sxs-lookup"><span data-stu-id="1c763-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="1c763-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c763-104">SYNTAX</span></span>

### <span data-ttu-id="1c763-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="1c763-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1c763-106">Lära</span><span class="sxs-lookup"><span data-stu-id="1c763-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1c763-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1c763-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1c763-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="1c763-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c763-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c763-109">DESCRIPTION</span></span>
<span data-ttu-id="1c763-110">Returnerar en BotService som anges av parametrarna.</span><span class="sxs-lookup"><span data-stu-id="1c763-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="1c763-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c763-111">EXAMPLES</span></span>

### <span data-ttu-id="1c763-112">Exempel 1: Hämta alla BotServices</span><span class="sxs-lookup"><span data-stu-id="1c763-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="1c763-113">Skaffa alla BotServices</span><span class="sxs-lookup"><span data-stu-id="1c763-113">Get all BotServices</span></span>

### <span data-ttu-id="1c763-114">Exempel 2: Hämta BotService genom ResourceGroupName och Name</span><span class="sxs-lookup"><span data-stu-id="1c763-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="1c763-115">Hämta BotService genom ResourceGroupName och namn</span><span class="sxs-lookup"><span data-stu-id="1c763-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="1c763-116">Exempel 3: Hämta alla BotServices genom ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c763-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="1c763-117">Skaffa alla BotServices genom ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c763-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="1c763-118">Exempel 4: Hämta BotService genom inputObject</span><span class="sxs-lookup"><span data-stu-id="1c763-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="1c763-119">Skaffa BotService genom inputObject</span><span class="sxs-lookup"><span data-stu-id="1c763-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="1c763-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c763-120">PARAMETERS</span></span>

### <span data-ttu-id="1c763-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c763-121">-DefaultProfile</span></span>
<span data-ttu-id="1c763-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c763-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c763-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c763-123">-InputObject</span></span>
<span data-ttu-id="1c763-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1c763-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c763-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c763-125">-Name</span></span>
<span data-ttu-id="1c763-126">Namnet på bot-resursen.</span><span class="sxs-lookup"><span data-stu-id="1c763-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c763-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c763-127">-ResourceGroupName</span></span>
<span data-ttu-id="1c763-128">Namnet på robot resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1c763-128">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c763-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c763-129">-SubscriptionId</span></span>
<span data-ttu-id="1c763-130">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1c763-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1c763-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c763-131">CommonParameters</span></span>
<span data-ttu-id="1c763-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c763-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c763-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c763-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c763-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c763-134">INPUTS</span></span>

### <span data-ttu-id="1c763-135">Microsoft. Azure. PowerShell. cmdletar. BotService. Models. IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="1c763-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="1c763-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c763-136">OUTPUTS</span></span>

### <span data-ttu-id="1c763-137">Microsoft. Azure. PowerShell. cmdletar. BotService. Models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="1c763-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="1c763-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c763-138">NOTES</span></span>

<span data-ttu-id="1c763-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1c763-139">ALIASES</span></span>

<span data-ttu-id="1c763-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="1c763-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c763-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="1c763-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c763-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c763-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c763-143">INPUTOBJECT <IBotServiceIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="1c763-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c763-144">`[ChannelName <ChannelName?>]`: Namnet på kanal resursen.</span><span class="sxs-lookup"><span data-stu-id="1c763-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="1c763-145">`[ConnectionName <String>]`: Namnet på resursen för bot tjänstens anslutnings inställning</span><span class="sxs-lookup"><span data-stu-id="1c763-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="1c763-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="1c763-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c763-147">`[ResourceGroupName <String>]`: Namnet på den här resurs gruppen för bot i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1c763-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="1c763-148">`[ResourceName <String>]`: Namnet på bot-resursen.</span><span class="sxs-lookup"><span data-stu-id="1c763-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="1c763-149">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1c763-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="1c763-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c763-150">RELATED LINKS</span></span>

