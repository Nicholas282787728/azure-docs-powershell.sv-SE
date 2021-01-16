---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413864"
---
# <span data-ttu-id="2975a-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="2975a-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="2975a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2975a-102">SYNOPSIS</span></span>
<span data-ttu-id="2975a-103">Ta bort en blockchain medlem.</span><span class="sxs-lookup"><span data-stu-id="2975a-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="2975a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2975a-104">SYNTAX</span></span>

### <span data-ttu-id="2975a-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="2975a-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2975a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2975a-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2975a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2975a-107">DESCRIPTION</span></span>
<span data-ttu-id="2975a-108">Ta bort en blockchain medlem.</span><span class="sxs-lookup"><span data-stu-id="2975a-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="2975a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2975a-109">EXAMPLES</span></span>

### <span data-ttu-id="2975a-110">Exempel 1: ta bort en blockchain medlem</span><span class="sxs-lookup"><span data-stu-id="2975a-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="2975a-111">Det här kommandot tar bort en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="2975a-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="2975a-112">Exempel 2: ta bort en blockchain medlem</span><span class="sxs-lookup"><span data-stu-id="2975a-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="2975a-113">Det här kommandot tar bort en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="2975a-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="2975a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2975a-114">PARAMETERS</span></span>

### <span data-ttu-id="2975a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2975a-115">-AsJob</span></span>
<span data-ttu-id="2975a-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="2975a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2975a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2975a-117">-DefaultProfile</span></span>
<span data-ttu-id="2975a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2975a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2975a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2975a-119">-InputObject</span></span>
<span data-ttu-id="2975a-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="2975a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2975a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2975a-121">-Name</span></span>
<span data-ttu-id="2975a-122">Blockchain medlems namn</span><span class="sxs-lookup"><span data-stu-id="2975a-122">Blockchain member name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2975a-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2975a-123">-NoWait</span></span>
<span data-ttu-id="2975a-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="2975a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2975a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2975a-125">-PassThru</span></span>
<span data-ttu-id="2975a-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="2975a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2975a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2975a-127">-ResourceGroupName</span></span>
<span data-ttu-id="2975a-128">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="2975a-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2975a-129">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="2975a-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2975a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2975a-130">-SubscriptionId</span></span>
<span data-ttu-id="2975a-131">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2975a-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2975a-132">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="2975a-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2975a-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2975a-133">-Confirm</span></span>
<span data-ttu-id="2975a-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2975a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2975a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2975a-135">-WhatIf</span></span>
<span data-ttu-id="2975a-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2975a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2975a-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2975a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2975a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2975a-138">CommonParameters</span></span>
<span data-ttu-id="2975a-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2975a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2975a-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2975a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2975a-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2975a-141">INPUTS</span></span>

### <span data-ttu-id="2975a-142">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="2975a-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="2975a-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2975a-143">OUTPUTS</span></span>

### <span data-ttu-id="2975a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2975a-144">System.Boolean</span></span>

## <span data-ttu-id="2975a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2975a-145">NOTES</span></span>

<span data-ttu-id="2975a-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2975a-146">ALIASES</span></span>

<span data-ttu-id="2975a-147">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="2975a-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2975a-148">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="2975a-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2975a-149">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2975a-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2975a-150">INPUTOBJECT <IBlockchainIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="2975a-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2975a-151">`[BlockchainMemberName <String>]`: Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="2975a-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="2975a-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="2975a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2975a-153">`[Location <String>]`: Plats namn.</span><span class="sxs-lookup"><span data-stu-id="2975a-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="2975a-154">`[OperationId <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="2975a-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="2975a-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="2975a-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2975a-156">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="2975a-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2975a-157">`[SubscriptionId <String>]`: Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2975a-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="2975a-158">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="2975a-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="2975a-159">`[TransactionNodeName <String>]`: Namn på nodnamn.</span><span class="sxs-lookup"><span data-stu-id="2975a-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="2975a-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2975a-160">RELATED LINKS</span></span>

