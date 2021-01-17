---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405920"
---
# <span data-ttu-id="55557-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="55557-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="55557-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55557-102">SYNOPSIS</span></span>
<span data-ttu-id="55557-103">Få information om en blockchain medlem.</span><span class="sxs-lookup"><span data-stu-id="55557-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="55557-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55557-104">SYNTAX</span></span>

### <span data-ttu-id="55557-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="55557-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="55557-106">Lära</span><span class="sxs-lookup"><span data-stu-id="55557-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="55557-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="55557-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="55557-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="55557-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="55557-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55557-109">DESCRIPTION</span></span>
<span data-ttu-id="55557-110">Få information om en blockchain medlem.</span><span class="sxs-lookup"><span data-stu-id="55557-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="55557-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55557-111">EXAMPLES</span></span>

### <span data-ttu-id="55557-112">Exempel 1: lista blockchain medlemmar</span><span class="sxs-lookup"><span data-stu-id="55557-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="55557-113">Det här kommandot listar blockchain medlemmar under ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="55557-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="55557-114">Exempel 2: lista blockchain medlemmar</span><span class="sxs-lookup"><span data-stu-id="55557-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="55557-115">Det här kommandot listar blockchain medlemmar under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="55557-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="55557-116">Exempel 3: skaffa en blockchain medlem</span><span class="sxs-lookup"><span data-stu-id="55557-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="55557-117">Det här kommandot får en blockchain medlem under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="55557-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="55557-118">Exempel 4: skaffa en blockchain medlem</span><span class="sxs-lookup"><span data-stu-id="55557-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="55557-119">Det här kommandot får en blockchain medlem under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="55557-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="55557-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55557-120">PARAMETERS</span></span>

### <span data-ttu-id="55557-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55557-121">-DefaultProfile</span></span>
<span data-ttu-id="55557-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55557-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55557-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55557-123">-InputObject</span></span>
<span data-ttu-id="55557-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="55557-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="55557-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="55557-125">-Name</span></span>
<span data-ttu-id="55557-126">Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="55557-126">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55557-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55557-127">-ResourceGroupName</span></span>
<span data-ttu-id="55557-128">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="55557-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="55557-129">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="55557-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="55557-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55557-130">-SubscriptionId</span></span>
<span data-ttu-id="55557-131">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="55557-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="55557-132">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="55557-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="55557-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55557-133">CommonParameters</span></span>
<span data-ttu-id="55557-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55557-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55557-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55557-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55557-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55557-136">INPUTS</span></span>

### <span data-ttu-id="55557-137">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="55557-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="55557-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55557-138">OUTPUTS</span></span>

### <span data-ttu-id="55557-139">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="55557-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="55557-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55557-140">NOTES</span></span>

<span data-ttu-id="55557-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="55557-141">ALIASES</span></span>

<span data-ttu-id="55557-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="55557-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55557-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="55557-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55557-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="55557-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55557-145">INPUTOBJECT <IBlockchainIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="55557-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="55557-146">`[BlockchainMemberName <String>]`: Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="55557-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="55557-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="55557-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="55557-148">`[Location <String>]`: Plats namn.</span><span class="sxs-lookup"><span data-stu-id="55557-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="55557-149">`[OperationId <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="55557-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="55557-150">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="55557-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="55557-151">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="55557-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="55557-152">`[SubscriptionId <String>]`: Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="55557-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="55557-153">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="55557-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="55557-154">`[TransactionNodeName <String>]`: Namn på nodnamn.</span><span class="sxs-lookup"><span data-stu-id="55557-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="55557-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55557-155">RELATED LINKS</span></span>

