---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089195"
---
# <span data-ttu-id="04ed8-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="04ed8-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="04ed8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="04ed8-103">Skapar en disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="04ed8-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="04ed8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04ed8-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ed8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04ed8-105">DESCRIPTION</span></span>
<span data-ttu-id="04ed8-106">Skapar en disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="04ed8-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="04ed8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04ed8-107">EXAMPLES</span></span>

### <span data-ttu-id="04ed8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="04ed8-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="04ed8-109">Skapar disk krypterings uppsättning med den angivna aktiva knappen i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="04ed8-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="04ed8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04ed8-110">PARAMETERS</span></span>

### <span data-ttu-id="04ed8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04ed8-111">-AsJob</span></span>
<span data-ttu-id="04ed8-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="04ed8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04ed8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ed8-113">-DefaultProfile</span></span>
<span data-ttu-id="04ed8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04ed8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04ed8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04ed8-115">-InputObject</span></span>
<span data-ttu-id="04ed8-116">Det lokala objektet i disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="04ed8-116">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="04ed8-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="04ed8-117">-Name</span></span>
<span data-ttu-id="04ed8-118">Namn på disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="04ed8-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="04ed8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ed8-119">-ResourceGroupName</span></span>
<span data-ttu-id="04ed8-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="04ed8-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="04ed8-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04ed8-121">-Confirm</span></span>
<span data-ttu-id="04ed8-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04ed8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04ed8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ed8-123">-WhatIf</span></span>
<span data-ttu-id="04ed8-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04ed8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04ed8-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04ed8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04ed8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ed8-126">CommonParameters</span></span>
<span data-ttu-id="04ed8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ed8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ed8-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04ed8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ed8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04ed8-129">INPUTS</span></span>

### <span data-ttu-id="04ed8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="04ed8-130">System.String</span></span>

### <span data-ttu-id="04ed8-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="04ed8-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="04ed8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04ed8-132">OUTPUTS</span></span>

### <span data-ttu-id="04ed8-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="04ed8-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="04ed8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04ed8-134">NOTES</span></span>

## <span data-ttu-id="04ed8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04ed8-135">RELATED LINKS</span></span>
