---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092315"
---
# <span data-ttu-id="57ced-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="57ced-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="57ced-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57ced-102">SYNOPSIS</span></span>
<span data-ttu-id="57ced-103">Uppdaterar en disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="57ced-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="57ced-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57ced-104">SYNTAX</span></span>

### <span data-ttu-id="57ced-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="57ced-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57ced-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="57ced-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57ced-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="57ced-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57ced-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57ced-108">DESCRIPTION</span></span>
<span data-ttu-id="57ced-109">Uppdaterar en disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="57ced-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="57ced-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57ced-110">EXAMPLES</span></span>

### <span data-ttu-id="57ced-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="57ced-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="57ced-112">Uppdaterar disk krypterings uppsättning med den angivna aktiva knappen i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="57ced-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="57ced-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57ced-113">PARAMETERS</span></span>

### <span data-ttu-id="57ced-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57ced-114">-AsJob</span></span>
<span data-ttu-id="57ced-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="57ced-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57ced-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ced-116">-DefaultProfile</span></span>
<span data-ttu-id="57ced-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57ced-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57ced-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57ced-118">-InputObject</span></span>
<span data-ttu-id="57ced-119">Det lokala objektet i disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="57ced-119">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57ced-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="57ced-120">-KeyUrl</span></span>
<span data-ttu-id="57ced-121">URL som pekar på den aktiva knappen i ett valv</span><span class="sxs-lookup"><span data-stu-id="57ced-121">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57ced-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="57ced-122">-Name</span></span>
<span data-ttu-id="57ced-123">Namn på disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="57ced-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57ced-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ced-124">-ResourceGroupName</span></span>
<span data-ttu-id="57ced-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="57ced-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57ced-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57ced-126">-ResourceId</span></span>
<span data-ttu-id="57ced-127">ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="57ced-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57ced-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="57ced-128">-SourceVaultId</span></span>
<span data-ttu-id="57ced-129">Resurs-ID för det valv som innehåller den aktiva tangenten.</span><span class="sxs-lookup"><span data-stu-id="57ced-129">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57ced-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="57ced-130">-Tag</span></span>
<span data-ttu-id="57ced-131">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="57ced-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="57ced-132">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="57ced-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57ced-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="57ced-133">-Confirm</span></span>
<span data-ttu-id="57ced-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="57ced-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57ced-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57ced-135">-WhatIf</span></span>
<span data-ttu-id="57ced-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="57ced-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57ced-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="57ced-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57ced-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ced-138">CommonParameters</span></span>
<span data-ttu-id="57ced-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ced-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ced-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57ced-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ced-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57ced-141">INPUTS</span></span>

### <span data-ttu-id="57ced-142">System. String</span><span class="sxs-lookup"><span data-stu-id="57ced-142">System.String</span></span>

### <span data-ttu-id="57ced-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="57ced-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="57ced-144">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="57ced-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="57ced-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57ced-145">OUTPUTS</span></span>

### <span data-ttu-id="57ced-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="57ced-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="57ced-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57ced-147">NOTES</span></span>

## <span data-ttu-id="57ced-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57ced-148">RELATED LINKS</span></span>
