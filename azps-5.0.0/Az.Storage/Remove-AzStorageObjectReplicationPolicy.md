---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269034"
---
# <span data-ttu-id="8eda1-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="8eda1-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="8eda1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8eda1-102">SYNOPSIS</span></span>
<span data-ttu-id="8eda1-103">Tar bort den angivna resursallokeringsprincipen från ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="8eda1-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="8eda1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8eda1-104">SYNTAX</span></span>

### <span data-ttu-id="8eda1-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="8eda1-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8eda1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8eda1-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eda1-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="8eda1-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eda1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8eda1-108">DESCRIPTION</span></span>
<span data-ttu-id="8eda1-109">Cmdleten **Remove-AzStorageObjectReplicationPolicy** tar bort den angivna resursallokeringsprincipen från ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="8eda1-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="8eda1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8eda1-110">EXAMPLES</span></span>

### <span data-ttu-id="8eda1-111">Exempel 1: ta bort en resursallokeringsprincip med specifika policyId från ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="8eda1-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="8eda1-112">Det här kommandot tar bort en resursallokeringsprincip med specifika policyId från ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="8eda1-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="8eda1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8eda1-113">PARAMETERS</span></span>

### <span data-ttu-id="8eda1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eda1-114">-DefaultProfile</span></span>
<span data-ttu-id="8eda1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8eda1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eda1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8eda1-116">-InputObject</span></span>
<span data-ttu-id="8eda1-117">Principobjektet objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8eda1-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="8eda1-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8eda1-118">-PassThru</span></span>
<span data-ttu-id="8eda1-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8eda1-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8eda1-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="8eda1-120">-PolicyId</span></span>
<span data-ttu-id="8eda1-121">ID för principobjektet för objekt.</span><span class="sxs-lookup"><span data-stu-id="8eda1-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="8eda1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eda1-122">-ResourceGroupName</span></span>
<span data-ttu-id="8eda1-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="8eda1-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eda1-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eda1-124">-StorageAccount</span></span>
<span data-ttu-id="8eda1-125">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="8eda1-125">Storage account object</span></span>

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

### <span data-ttu-id="8eda1-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8eda1-126">-StorageAccountName</span></span>
<span data-ttu-id="8eda1-127">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="8eda1-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eda1-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8eda1-128">-Confirm</span></span>
<span data-ttu-id="8eda1-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8eda1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eda1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eda1-130">-WhatIf</span></span>
<span data-ttu-id="8eda1-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8eda1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eda1-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8eda1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eda1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eda1-133">CommonParameters</span></span>
<span data-ttu-id="8eda1-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eda1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eda1-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eda1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eda1-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8eda1-136">INPUTS</span></span>

### <span data-ttu-id="8eda1-137">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eda1-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8eda1-138">Microsoft. Azure. commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="8eda1-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="8eda1-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8eda1-139">OUTPUTS</span></span>

### <span data-ttu-id="8eda1-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8eda1-140">System.Boolean</span></span>

## <span data-ttu-id="8eda1-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8eda1-141">NOTES</span></span>

## <span data-ttu-id="8eda1-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8eda1-142">RELATED LINKS</span></span>
