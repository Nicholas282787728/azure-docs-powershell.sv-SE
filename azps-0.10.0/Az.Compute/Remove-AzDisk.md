---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: 9e3a194d1143134b1ba3aa472db61062baf847f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924998"
---
# <span data-ttu-id="ff5ff-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="ff5ff-101">Remove-AzDisk</span></span>

## <span data-ttu-id="ff5ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5ff-103">Tar bort en disk.</span><span class="sxs-lookup"><span data-stu-id="ff5ff-103">Removes a disk.</span></span>

## <span data-ttu-id="ff5ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff5ff-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff5ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff5ff-105">DESCRIPTION</span></span>
<span data-ttu-id="ff5ff-106">Cmdleten **Remove-AzDisk** tar bort en disk.</span><span class="sxs-lookup"><span data-stu-id="ff5ff-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="ff5ff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff5ff-107">EXAMPLES</span></span>

### <span data-ttu-id="ff5ff-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ff5ff-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="ff5ff-109">Det här kommandot tar bort disken "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ff5ff-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ff5ff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff5ff-110">PARAMETERS</span></span>

### <span data-ttu-id="ff5ff-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff5ff-111">-AsJob</span></span>
<span data-ttu-id="ff5ff-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="ff5ff-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff5ff-113">-DefaultProfile</span></span>
<span data-ttu-id="ff5ff-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff5ff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5ff-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ff5ff-115">-DiskName</span></span>
<span data-ttu-id="ff5ff-116">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="ff5ff-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff5ff-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ff5ff-117">-Force</span></span>
<span data-ttu-id="ff5ff-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ff5ff-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5ff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff5ff-119">-ResourceGroupName</span></span>
<span data-ttu-id="ff5ff-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ff5ff-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff5ff-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff5ff-121">-Confirm</span></span>
<span data-ttu-id="ff5ff-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff5ff-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5ff-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff5ff-123">-WhatIf</span></span>
<span data-ttu-id="ff5ff-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff5ff-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff5ff-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff5ff-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5ff-126">CommonParameters</span></span>
<span data-ttu-id="ff5ff-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff5ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff5ff-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff5ff-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5ff-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff5ff-129">INPUTS</span></span>

### <span data-ttu-id="ff5ff-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ff5ff-130">System.String</span></span>

## <span data-ttu-id="ff5ff-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff5ff-131">OUTPUTS</span></span>

### <span data-ttu-id="ff5ff-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="ff5ff-132">System.Object</span></span>

## <span data-ttu-id="ff5ff-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff5ff-133">NOTES</span></span>

## <span data-ttu-id="ff5ff-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff5ff-134">RELATED LINKS</span></span>

