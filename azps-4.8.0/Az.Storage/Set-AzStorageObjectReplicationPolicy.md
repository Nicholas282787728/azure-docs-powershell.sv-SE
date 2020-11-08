---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259780"
---
# <span data-ttu-id="b26c3-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="b26c3-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="b26c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b26c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b26c3-103">Skapar eller uppdaterar den angivna resursallokeringsprincipen i ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b26c3-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="b26c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b26c3-104">SYNTAX</span></span>

### <span data-ttu-id="b26c3-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="b26c3-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b26c3-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="b26c3-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b26c3-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b26c3-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b26c3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b26c3-108">DESCRIPTION</span></span>
<span data-ttu-id="b26c3-109">Cmdleten **set-AzStorageObjectReplicationPolicy** skapar eller uppdaterar den angivna resursallokeringsprincipen i ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b26c3-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="b26c3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b26c3-110">EXAMPLES</span></span>

### <span data-ttu-id="b26c3-111">Exempel 1: Ange princip för lösenordsreplikering till både mål-och käll konto.</span><span class="sxs-lookup"><span data-stu-id="b26c3-111">Example 1: Set object replication policy to both destination and source account.</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $destPolicy = Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId default -SourceAccount $srcAccountName  -Rule $rule1,$rule2

PS C:\> $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mysourceaccount" -InputObject $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----                                     
myresourcegroup   mysourceaccount    56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
```

<span data-ttu-id="b26c3-112">Det här kommandot anger princip för lösenordsreplikering till både mål-och käll konto.</span><span class="sxs-lookup"><span data-stu-id="b26c3-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="b26c3-113">Skapa först två regler för replikeringsprinciper och ange en princip med de två reglerna till destinations konto.</span><span class="sxs-lookup"><span data-stu-id="b26c3-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="b26c3-114">Ange sedan lösenordsreplikeringsprincip från mål kontot till käll konto.</span><span class="sxs-lookup"><span data-stu-id="b26c3-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="b26c3-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b26c3-115">PARAMETERS</span></span>

### <span data-ttu-id="b26c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26c3-116">-DefaultProfile</span></span>
<span data-ttu-id="b26c3-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b26c3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26c3-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="b26c3-118">-DestinationAccount</span></span>
<span data-ttu-id="b26c3-119">DestinationAccount för princip för objekt.</span><span class="sxs-lookup"><span data-stu-id="b26c3-119">Object Replication Policy DestinationAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26c3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b26c3-120">-InputObject</span></span>
<span data-ttu-id="b26c3-121">Objektet för lösenordsreplikeringsprincip för att ange angivet konto.</span><span class="sxs-lookup"><span data-stu-id="b26c3-121">Object Replication Policy Object to Set to the specified Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b26c3-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="b26c3-122">-PolicyId</span></span>
<span data-ttu-id="b26c3-123">ID för principobjektet för objekt. Det ska vara ett GUID eller "default".</span><span class="sxs-lookup"><span data-stu-id="b26c3-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="b26c3-124">Om du inte anger PolicyId, använder "default", vilket betyder att du ska skapa en ny princip och ID: t för den nya principen returneras i den policy som skapas.</span><span class="sxs-lookup"><span data-stu-id="b26c3-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26c3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b26c3-125">-ResourceGroupName</span></span>
<span data-ttu-id="b26c3-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b26c3-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26c3-127">-Regel</span><span class="sxs-lookup"><span data-stu-id="b26c3-127">-Rule</span></span>
<span data-ttu-id="b26c3-128">Regler för lösenordsreplikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="b26c3-128">Object Replication Policy Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule[]
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26c3-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="b26c3-129">-SourceAccount</span></span>
<span data-ttu-id="b26c3-130">SourceAccount för princip för objekt.</span><span class="sxs-lookup"><span data-stu-id="b26c3-130">Object Replication Policy SourceAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26c3-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b26c3-131">-StorageAccount</span></span>
<span data-ttu-id="b26c3-132">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="b26c3-132">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b26c3-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b26c3-133">-StorageAccountName</span></span>
<span data-ttu-id="b26c3-134">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b26c3-134">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26c3-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b26c3-135">-Confirm</span></span>
<span data-ttu-id="b26c3-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b26c3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b26c3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b26c3-137">-WhatIf</span></span>
<span data-ttu-id="b26c3-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b26c3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b26c3-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b26c3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b26c3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26c3-140">CommonParameters</span></span>
<span data-ttu-id="b26c3-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b26c3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26c3-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b26c3-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26c3-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b26c3-143">INPUTS</span></span>

### <span data-ttu-id="b26c3-144">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b26c3-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b26c3-145">Microsoft. Azure. commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="b26c3-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="b26c3-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b26c3-146">OUTPUTS</span></span>

### <span data-ttu-id="b26c3-147">Microsoft. Azure. commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="b26c3-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="b26c3-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b26c3-148">NOTES</span></span>

## <span data-ttu-id="b26c3-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b26c3-149">RELATED LINKS</span></span>
