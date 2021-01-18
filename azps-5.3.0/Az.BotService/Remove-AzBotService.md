---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: ef75ec3e48a68bffce7c5b281f542bd2e3dba9d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524642"
---
# <span data-ttu-id="40f3c-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="40f3c-101">Remove-AzBotService</span></span>

## <span data-ttu-id="40f3c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="40f3c-103">Tar bort en bot-tjänst från resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="40f3c-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="40f3c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40f3c-104">SYNTAX</span></span>

### <span data-ttu-id="40f3c-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="40f3c-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="40f3c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="40f3c-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40f3c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40f3c-107">DESCRIPTION</span></span>
<span data-ttu-id="40f3c-108">Tar bort en bot-tjänst från resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="40f3c-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="40f3c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40f3c-109">EXAMPLES</span></span>

### <span data-ttu-id="40f3c-110">Exempel 1: ta bort BotService med namn och ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f3c-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="40f3c-111">Ta bort BotService efter namn och ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f3c-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="40f3c-112">Exempel 2: ta bort BotService med InputObject</span><span class="sxs-lookup"><span data-stu-id="40f3c-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="40f3c-113">Ta bort BotService med InputObject</span><span class="sxs-lookup"><span data-stu-id="40f3c-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="40f3c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40f3c-114">PARAMETERS</span></span>

### <span data-ttu-id="40f3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f3c-115">-DefaultProfile</span></span>
<span data-ttu-id="40f3c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40f3c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40f3c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40f3c-117">-InputObject</span></span>
<span data-ttu-id="40f3c-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="40f3c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40f3c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="40f3c-119">-Name</span></span>
<span data-ttu-id="40f3c-120">Namnet på bot-resursen.</span><span class="sxs-lookup"><span data-stu-id="40f3c-120">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f3c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40f3c-121">-PassThru</span></span>
<span data-ttu-id="40f3c-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="40f3c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="40f3c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f3c-123">-ResourceGroupName</span></span>
<span data-ttu-id="40f3c-124">Namnet på robot resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="40f3c-124">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f3c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40f3c-125">-SubscriptionId</span></span>
<span data-ttu-id="40f3c-126">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="40f3c-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f3c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="40f3c-127">-Confirm</span></span>
<span data-ttu-id="40f3c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="40f3c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40f3c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40f3c-129">-WhatIf</span></span>
<span data-ttu-id="40f3c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="40f3c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40f3c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="40f3c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40f3c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f3c-132">CommonParameters</span></span>
<span data-ttu-id="40f3c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40f3c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f3c-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40f3c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f3c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40f3c-135">INPUTS</span></span>

### <span data-ttu-id="40f3c-136">Microsoft. Azure. PowerShell. cmdletar. BotService. Models. IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="40f3c-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="40f3c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40f3c-137">OUTPUTS</span></span>

### <span data-ttu-id="40f3c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40f3c-138">System.Boolean</span></span>

## <span data-ttu-id="40f3c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40f3c-139">NOTES</span></span>

<span data-ttu-id="40f3c-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="40f3c-140">ALIASES</span></span>

<span data-ttu-id="40f3c-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="40f3c-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40f3c-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="40f3c-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40f3c-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40f3c-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40f3c-144">INPUTOBJECT <IBotServiceIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="40f3c-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="40f3c-145">`[ChannelName <ChannelName?>]`: Namnet på kanal resursen.</span><span class="sxs-lookup"><span data-stu-id="40f3c-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="40f3c-146">`[ConnectionName <String>]`: Namnet på resursen för bot tjänstens anslutnings inställning</span><span class="sxs-lookup"><span data-stu-id="40f3c-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="40f3c-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="40f3c-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="40f3c-148">`[ResourceGroupName <String>]`: Namnet på den här resurs gruppen för bot i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="40f3c-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="40f3c-149">`[ResourceName <String>]`: Namnet på bot-resursen.</span><span class="sxs-lookup"><span data-stu-id="40f3c-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="40f3c-150">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="40f3c-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="40f3c-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40f3c-151">RELATED LINKS</span></span>

