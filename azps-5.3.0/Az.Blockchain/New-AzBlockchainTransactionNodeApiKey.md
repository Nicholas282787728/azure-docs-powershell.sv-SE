---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524673"
---
# <span data-ttu-id="301eb-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="301eb-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="301eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="301eb-102">SYNOPSIS</span></span>
<span data-ttu-id="301eb-103">Återskapa API-nycklarna för blockchain-medlemmen.</span><span class="sxs-lookup"><span data-stu-id="301eb-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="301eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="301eb-104">SYNTAX</span></span>

### <span data-ttu-id="301eb-105">RegenerateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="301eb-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="301eb-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="301eb-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="301eb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="301eb-107">DESCRIPTION</span></span>
<span data-ttu-id="301eb-108">Återskapa API-nycklarna för blockchain-medlemmen.</span><span class="sxs-lookup"><span data-stu-id="301eb-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="301eb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="301eb-109">EXAMPLES</span></span>

### <span data-ttu-id="301eb-110">Exempel 1: återskapa API-nycklar för en Artikelnod med hjälp av namn.</span><span class="sxs-lookup"><span data-stu-id="301eb-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="301eb-111">Det här kommandot skapar API-nycklar för en Artikelnod med hjälp av namn, resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="301eb-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="301eb-112">Exempel 2: återskapa API-nycklar för en Artikelnod</span><span class="sxs-lookup"><span data-stu-id="301eb-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="301eb-113">Det här kommandot genererar API-nycklar för en Transaction-nod med Idenity.</span><span class="sxs-lookup"><span data-stu-id="301eb-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="301eb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="301eb-114">PARAMETERS</span></span>

### <span data-ttu-id="301eb-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="301eb-115">-BlockchainMemberName</span></span>
<span data-ttu-id="301eb-116">Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="301eb-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="301eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301eb-117">-DefaultProfile</span></span>
<span data-ttu-id="301eb-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="301eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="301eb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="301eb-119">-InputObject</span></span>
<span data-ttu-id="301eb-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="301eb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="301eb-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="301eb-121">-KeyName</span></span>
<span data-ttu-id="301eb-122">Hämtar eller anger API-namnet.</span><span class="sxs-lookup"><span data-stu-id="301eb-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="301eb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301eb-123">-ResourceGroupName</span></span>
<span data-ttu-id="301eb-124">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="301eb-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="301eb-125">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="301eb-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="301eb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="301eb-126">-SubscriptionId</span></span>
<span data-ttu-id="301eb-127">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="301eb-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="301eb-128">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="301eb-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="301eb-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="301eb-129">-TransactionNodeName</span></span>
<span data-ttu-id="301eb-130">Nodnamn för transaktion.</span><span class="sxs-lookup"><span data-stu-id="301eb-130">Transaction node name.</span></span>

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

### <span data-ttu-id="301eb-131">-Värde</span><span class="sxs-lookup"><span data-stu-id="301eb-131">-Value</span></span>
<span data-ttu-id="301eb-132">Hämtar eller anger API-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="301eb-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="301eb-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="301eb-133">-Confirm</span></span>
<span data-ttu-id="301eb-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="301eb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="301eb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301eb-135">-WhatIf</span></span>
<span data-ttu-id="301eb-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="301eb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="301eb-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="301eb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="301eb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301eb-138">CommonParameters</span></span>
<span data-ttu-id="301eb-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="301eb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301eb-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="301eb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301eb-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="301eb-141">INPUTS</span></span>

### <span data-ttu-id="301eb-142">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="301eb-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="301eb-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="301eb-143">OUTPUTS</span></span>

### <span data-ttu-id="301eb-144">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="301eb-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="301eb-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="301eb-145">NOTES</span></span>

<span data-ttu-id="301eb-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="301eb-146">ALIASES</span></span>

<span data-ttu-id="301eb-147">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="301eb-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="301eb-148">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="301eb-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="301eb-149">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="301eb-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="301eb-150">INPUTOBJECT <IBlockchainIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="301eb-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="301eb-151">`[BlockchainMemberName <String>]`: Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="301eb-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="301eb-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="301eb-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="301eb-153">`[Location <String>]`: Plats namn.</span><span class="sxs-lookup"><span data-stu-id="301eb-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="301eb-154">`[OperationId <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="301eb-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="301eb-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="301eb-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="301eb-156">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="301eb-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="301eb-157">`[SubscriptionId <String>]`: Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="301eb-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="301eb-158">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="301eb-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="301eb-159">`[TransactionNodeName <String>]`: Namn på nodnamn.</span><span class="sxs-lookup"><span data-stu-id="301eb-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="301eb-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="301eb-160">RELATED LINKS</span></span>

