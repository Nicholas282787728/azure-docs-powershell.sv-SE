---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258902"
---
# <span data-ttu-id="cb156-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cb156-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="cb156-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb156-102">SYNOPSIS</span></span>
<span data-ttu-id="cb156-103">Skapar en disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="cb156-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="cb156-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb156-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb156-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb156-105">DESCRIPTION</span></span>
<span data-ttu-id="cb156-106">Skapar en disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="cb156-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="cb156-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb156-107">EXAMPLES</span></span>

### <span data-ttu-id="cb156-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cb156-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="cb156-109">Skapar disk krypterings uppsättning med den angivna aktiva knappen i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="cb156-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="cb156-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb156-110">PARAMETERS</span></span>

### <span data-ttu-id="cb156-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb156-111">-AsJob</span></span>
<span data-ttu-id="cb156-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cb156-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb156-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb156-113">-DefaultProfile</span></span>
<span data-ttu-id="cb156-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb156-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb156-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb156-115">-InputObject</span></span>
<span data-ttu-id="cb156-116">Det lokala objektet i disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="cb156-116">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: (All)
Aliases: DiskEncryptionSet

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb156-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb156-117">-Name</span></span>
<span data-ttu-id="cb156-118">Namn på disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="cb156-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb156-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb156-119">-ResourceGroupName</span></span>
<span data-ttu-id="cb156-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cb156-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb156-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb156-121">-Confirm</span></span>
<span data-ttu-id="cb156-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb156-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb156-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb156-123">-WhatIf</span></span>
<span data-ttu-id="cb156-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb156-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb156-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb156-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb156-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb156-126">CommonParameters</span></span>
<span data-ttu-id="cb156-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb156-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb156-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb156-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb156-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb156-129">INPUTS</span></span>

### <span data-ttu-id="cb156-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cb156-130">System.String</span></span>

### <span data-ttu-id="cb156-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cb156-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="cb156-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb156-132">OUTPUTS</span></span>

### <span data-ttu-id="cb156-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cb156-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="cb156-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb156-134">NOTES</span></span>

## <span data-ttu-id="cb156-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb156-135">RELATED LINKS</span></span>
