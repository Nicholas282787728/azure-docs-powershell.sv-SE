---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: bcfba4bb002d7982f9a0fb9220fbce24e12e6ffb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585731"
---
# <span data-ttu-id="05647-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="05647-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="05647-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05647-102">SYNOPSIS</span></span>
<span data-ttu-id="05647-103">Tar bort en disk.</span><span class="sxs-lookup"><span data-stu-id="05647-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05647-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05647-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05647-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05647-105">DESCRIPTION</span></span>
<span data-ttu-id="05647-106">Cmdleten **Remove-AzureRmDisk** tar bort en disk.</span><span class="sxs-lookup"><span data-stu-id="05647-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="05647-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05647-107">EXAMPLES</span></span>

### <span data-ttu-id="05647-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="05647-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="05647-109">Det här kommandot tar bort disken "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="05647-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="05647-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05647-110">PARAMETERS</span></span>

### <span data-ttu-id="05647-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05647-111">-DefaultProfile</span></span>
<span data-ttu-id="05647-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05647-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05647-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="05647-113">-DiskName</span></span>
<span data-ttu-id="05647-114">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="05647-114">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05647-115">-Force</span><span class="sxs-lookup"><span data-stu-id="05647-115">-Force</span></span>
<span data-ttu-id="05647-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="05647-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="05647-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05647-117">-ResourceGroupName</span></span>
<span data-ttu-id="05647-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="05647-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05647-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05647-119">-Confirm</span></span>
<span data-ttu-id="05647-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05647-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05647-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05647-121">-WhatIf</span></span>
<span data-ttu-id="05647-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05647-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05647-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05647-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05647-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05647-124">CommonParameters</span></span>
<span data-ttu-id="05647-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05647-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05647-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05647-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05647-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05647-127">INPUTS</span></span>

### <span data-ttu-id="05647-128">System. String</span><span class="sxs-lookup"><span data-stu-id="05647-128">System.String</span></span>

## <span data-ttu-id="05647-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05647-129">OUTPUTS</span></span>

### <span data-ttu-id="05647-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="05647-130">System.Object</span></span>

## <span data-ttu-id="05647-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05647-131">NOTES</span></span>

## <span data-ttu-id="05647-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05647-132">RELATED LINKS</span></span>
