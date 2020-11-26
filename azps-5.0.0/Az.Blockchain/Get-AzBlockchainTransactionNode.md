---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272780"
---
# <span data-ttu-id="12651-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="12651-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="12651-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12651-102">SYNOPSIS</span></span>
<span data-ttu-id="12651-103">Få information om noden Transaction.</span><span class="sxs-lookup"><span data-stu-id="12651-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="12651-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12651-104">SYNTAX</span></span>

### <span data-ttu-id="12651-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="12651-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="12651-106">Lära</span><span class="sxs-lookup"><span data-stu-id="12651-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="12651-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12651-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="12651-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12651-108">DESCRIPTION</span></span>
<span data-ttu-id="12651-109">Få information om noden Transaction.</span><span class="sxs-lookup"><span data-stu-id="12651-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="12651-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12651-110">EXAMPLES</span></span>

### <span data-ttu-id="12651-111">Exempel 1: lista över transaktionsloggfiler för en blockchain-medlem</span><span class="sxs-lookup"><span data-stu-id="12651-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="12651-112">Det här kommandot visar transaktionsloggfiler för en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="12651-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="12651-113">Exempel 2: Hämta en serverklusternod</span><span class="sxs-lookup"><span data-stu-id="12651-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="12651-114">Det här kommandot får en Transaction-nod.</span><span class="sxs-lookup"><span data-stu-id="12651-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="12651-115">Exempel 3: Hämta en serverklusternod</span><span class="sxs-lookup"><span data-stu-id="12651-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="12651-116">Det här kommandot får en Transaction-nod.</span><span class="sxs-lookup"><span data-stu-id="12651-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="12651-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12651-117">PARAMETERS</span></span>

### <span data-ttu-id="12651-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="12651-118">-BlockchainMemberName</span></span>
<span data-ttu-id="12651-119">Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="12651-119">Blockchain member name.</span></span>

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

### <span data-ttu-id="12651-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12651-120">-DefaultProfile</span></span>
<span data-ttu-id="12651-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12651-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12651-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12651-122">-InputObject</span></span>
<span data-ttu-id="12651-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="12651-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12651-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="12651-124">-Name</span></span>
<span data-ttu-id="12651-125">Nodnamn för transaktion.</span><span class="sxs-lookup"><span data-stu-id="12651-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12651-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12651-126">-ResourceGroupName</span></span>
<span data-ttu-id="12651-127">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="12651-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="12651-128">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="12651-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="12651-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12651-129">-SubscriptionId</span></span>
<span data-ttu-id="12651-130">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="12651-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="12651-131">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="12651-131">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12651-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12651-132">CommonParameters</span></span>
<span data-ttu-id="12651-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12651-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12651-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12651-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12651-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12651-135">INPUTS</span></span>

### <span data-ttu-id="12651-136">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="12651-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="12651-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12651-137">OUTPUTS</span></span>

### <span data-ttu-id="12651-138">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="12651-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="12651-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12651-139">NOTES</span></span>

<span data-ttu-id="12651-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="12651-140">ALIASES</span></span>

<span data-ttu-id="12651-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="12651-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12651-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="12651-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12651-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12651-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12651-144">INPUTOBJECT <IBlockchainIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="12651-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12651-145">`[BlockchainMemberName <String>]`: Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="12651-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="12651-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="12651-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12651-147">`[Location <String>]`: Plats namn.</span><span class="sxs-lookup"><span data-stu-id="12651-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="12651-148">`[OperationId <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="12651-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="12651-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="12651-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="12651-150">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="12651-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="12651-151">`[SubscriptionId <String>]`: Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="12651-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="12651-152">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="12651-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="12651-153">`[TransactionNodeName <String>]`: Namn på nodnamn.</span><span class="sxs-lookup"><span data-stu-id="12651-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="12651-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12651-154">RELATED LINKS</span></span>
