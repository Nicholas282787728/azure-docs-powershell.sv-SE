---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412624"
---
# <span data-ttu-id="3fa31-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="3fa31-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="3fa31-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3fa31-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa31-103">Ta bort Transaction-noden.</span><span class="sxs-lookup"><span data-stu-id="3fa31-103">Delete the transaction node.</span></span>

## <span data-ttu-id="3fa31-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3fa31-104">SYNTAX</span></span>

### <span data-ttu-id="3fa31-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="3fa31-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3fa31-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3fa31-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3fa31-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3fa31-107">DESCRIPTION</span></span>
<span data-ttu-id="3fa31-108">Ta bort Transaction-noden.</span><span class="sxs-lookup"><span data-stu-id="3fa31-108">Delete the transaction node.</span></span>

## <span data-ttu-id="3fa31-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3fa31-109">EXAMPLES</span></span>

### <span data-ttu-id="3fa31-110">Exempel 1: ta bort en serverklusternod</span><span class="sxs-lookup"><span data-stu-id="3fa31-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="3fa31-111">Det här kommandot tar bort en Transaction-nod.</span><span class="sxs-lookup"><span data-stu-id="3fa31-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="3fa31-112">Exempel 2: ta bort en transaktionskö</span><span class="sxs-lookup"><span data-stu-id="3fa31-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="3fa31-113">Det här kommandot tar bort en Transaction-nod.</span><span class="sxs-lookup"><span data-stu-id="3fa31-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="3fa31-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3fa31-114">PARAMETERS</span></span>

### <span data-ttu-id="3fa31-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fa31-115">-AsJob</span></span>
<span data-ttu-id="3fa31-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="3fa31-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3fa31-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="3fa31-117">-BlockchainMemberName</span></span>
<span data-ttu-id="3fa31-118">Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="3fa31-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="3fa31-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa31-119">-DefaultProfile</span></span>
<span data-ttu-id="3fa31-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3fa31-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fa31-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fa31-121">-InputObject</span></span>
<span data-ttu-id="3fa31-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3fa31-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa31-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="3fa31-123">-Name</span></span>
<span data-ttu-id="3fa31-124">Nodnamn för transaktion.</span><span class="sxs-lookup"><span data-stu-id="3fa31-124">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fa31-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3fa31-125">-NoWait</span></span>
<span data-ttu-id="3fa31-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="3fa31-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3fa31-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fa31-127">-PassThru</span></span>
<span data-ttu-id="3fa31-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="3fa31-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3fa31-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa31-129">-ResourceGroupName</span></span>
<span data-ttu-id="3fa31-130">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="3fa31-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3fa31-131">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="3fa31-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3fa31-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3fa31-132">-SubscriptionId</span></span>
<span data-ttu-id="3fa31-133">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3fa31-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3fa31-134">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3fa31-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3fa31-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3fa31-135">-Confirm</span></span>
<span data-ttu-id="3fa31-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3fa31-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fa31-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fa31-137">-WhatIf</span></span>
<span data-ttu-id="3fa31-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3fa31-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fa31-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3fa31-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fa31-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa31-140">CommonParameters</span></span>
<span data-ttu-id="3fa31-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fa31-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa31-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fa31-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa31-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3fa31-143">INPUTS</span></span>

### <span data-ttu-id="3fa31-144">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="3fa31-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="3fa31-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3fa31-145">OUTPUTS</span></span>

### <span data-ttu-id="3fa31-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3fa31-146">System.Boolean</span></span>

## <span data-ttu-id="3fa31-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3fa31-147">NOTES</span></span>

<span data-ttu-id="3fa31-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3fa31-148">ALIASES</span></span>

<span data-ttu-id="3fa31-149">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="3fa31-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3fa31-150">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="3fa31-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3fa31-151">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3fa31-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3fa31-152">INPUTOBJECT <IBlockchainIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="3fa31-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3fa31-153">`[BlockchainMemberName <String>]`: Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="3fa31-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="3fa31-154">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="3fa31-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3fa31-155">`[Location <String>]`: Plats namn.</span><span class="sxs-lookup"><span data-stu-id="3fa31-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="3fa31-156">`[OperationId <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="3fa31-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="3fa31-157">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="3fa31-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3fa31-158">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="3fa31-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3fa31-159">`[SubscriptionId <String>]`: Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3fa31-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="3fa31-160">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3fa31-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="3fa31-161">`[TransactionNodeName <String>]`: Namn på nodnamn.</span><span class="sxs-lookup"><span data-stu-id="3fa31-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="3fa31-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3fa31-162">RELATED LINKS</span></span>

