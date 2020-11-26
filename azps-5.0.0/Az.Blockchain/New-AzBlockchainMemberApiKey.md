---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323412"
---
# <span data-ttu-id="00366-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="00366-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="00366-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00366-102">SYNOPSIS</span></span>
<span data-ttu-id="00366-103">Återskapa API-nycklarna för en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="00366-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="00366-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00366-104">SYNTAX</span></span>

### <span data-ttu-id="00366-105">RegenerateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="00366-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="00366-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="00366-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="00366-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00366-107">DESCRIPTION</span></span>
<span data-ttu-id="00366-108">Återskapa API-nycklarna för en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="00366-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="00366-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00366-109">EXAMPLES</span></span>

### <span data-ttu-id="00366-110">Exempel 1: återskapa API-nycklar för en blockchain-medlem med namn</span><span class="sxs-lookup"><span data-stu-id="00366-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="00366-111">Det här kommandot återskapar API-nycklar för en blockchain-medlem med namn, resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="00366-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="00366-112">Exempel 2: återskapa API-nycklar för en blockchain-medlem med Idenity</span><span class="sxs-lookup"><span data-stu-id="00366-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="00366-113">Det här kommandot återskapar API-nycklar för en blockchain-medlem med identitet.</span><span class="sxs-lookup"><span data-stu-id="00366-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="00366-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00366-114">PARAMETERS</span></span>

### <span data-ttu-id="00366-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="00366-115">-BlockchainMemberName</span></span>
<span data-ttu-id="00366-116">Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="00366-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="00366-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00366-117">-DefaultProfile</span></span>
<span data-ttu-id="00366-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="00366-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00366-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00366-119">-InputObject</span></span>
<span data-ttu-id="00366-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="00366-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00366-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="00366-121">-KeyName</span></span>
<span data-ttu-id="00366-122">Hämtar eller anger API-namnet.</span><span class="sxs-lookup"><span data-stu-id="00366-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="00366-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00366-123">-ResourceGroupName</span></span>
<span data-ttu-id="00366-124">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="00366-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="00366-125">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="00366-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="00366-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00366-126">-SubscriptionId</span></span>
<span data-ttu-id="00366-127">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="00366-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="00366-128">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="00366-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="00366-129">-Värde</span><span class="sxs-lookup"><span data-stu-id="00366-129">-Value</span></span>
<span data-ttu-id="00366-130">Hämtar eller anger API-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="00366-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="00366-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="00366-131">-Confirm</span></span>
<span data-ttu-id="00366-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="00366-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00366-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00366-133">-WhatIf</span></span>
<span data-ttu-id="00366-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="00366-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00366-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="00366-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00366-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00366-136">CommonParameters</span></span>
<span data-ttu-id="00366-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00366-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00366-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00366-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00366-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00366-139">INPUTS</span></span>

### <span data-ttu-id="00366-140">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="00366-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="00366-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00366-141">OUTPUTS</span></span>

### <span data-ttu-id="00366-142">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="00366-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="00366-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00366-143">NOTES</span></span>

<span data-ttu-id="00366-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="00366-144">ALIASES</span></span>

<span data-ttu-id="00366-145">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="00366-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="00366-146">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="00366-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="00366-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="00366-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="00366-148">INPUTOBJECT <IBlockchainIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="00366-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="00366-149">`[BlockchainMemberName <String>]`: Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="00366-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="00366-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="00366-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="00366-151">`[Location <String>]`: Plats namn.</span><span class="sxs-lookup"><span data-stu-id="00366-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="00366-152">`[OperationId <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="00366-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="00366-153">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="00366-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="00366-154">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="00366-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="00366-155">`[SubscriptionId <String>]`: Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="00366-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="00366-156">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="00366-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="00366-157">`[TransactionNodeName <String>]`: Namn på nodnamn.</span><span class="sxs-lookup"><span data-stu-id="00366-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="00366-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00366-158">RELATED LINKS</span></span>
