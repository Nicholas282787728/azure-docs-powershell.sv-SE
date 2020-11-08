---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 39565aa0675a0afc5f6f3996cad522b435a1a9b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258909"
---
# <span data-ttu-id="5e073-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="5e073-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="5e073-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e073-102">SYNOPSIS</span></span>
<span data-ttu-id="5e073-103">Ger åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="5e073-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="5e073-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e073-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e073-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e073-105">DESCRIPTION</span></span>
<span data-ttu-id="5e073-106">**Grant-AzDiskAccess** cmdlet ger en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="5e073-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="5e073-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e073-107">EXAMPLES</span></span>

### <span data-ttu-id="5e073-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5e073-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="5e073-109">Ge "Read"-åtkomst till disken med namnet "Disk01" i resurs gruppen med namnet "ResourceGroup01" för 60 sekunder.</span><span class="sxs-lookup"><span data-stu-id="5e073-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="5e073-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e073-110">PARAMETERS</span></span>

### <span data-ttu-id="5e073-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="5e073-111">-Access</span></span>
<span data-ttu-id="5e073-112">Anger åtkomst nivå.</span><span class="sxs-lookup"><span data-stu-id="5e073-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e073-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e073-113">-AsJob</span></span>
<span data-ttu-id="5e073-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5e073-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e073-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e073-115">-DefaultProfile</span></span>
<span data-ttu-id="5e073-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e073-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e073-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="5e073-117">-DiskName</span></span>
<span data-ttu-id="5e073-118">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="5e073-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e073-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="5e073-119">-DurationInSecond</span></span>
<span data-ttu-id="5e073-120">Anger åtkomst längd i sekunder.</span><span class="sxs-lookup"><span data-stu-id="5e073-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e073-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e073-121">-ResourceGroupName</span></span>
<span data-ttu-id="5e073-122">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5e073-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5e073-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e073-123">-Confirm</span></span>
<span data-ttu-id="5e073-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e073-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e073-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e073-125">-WhatIf</span></span>
<span data-ttu-id="5e073-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e073-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e073-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e073-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e073-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e073-128">CommonParameters</span></span>
<span data-ttu-id="5e073-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e073-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e073-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e073-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e073-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e073-131">INPUTS</span></span>

### <span data-ttu-id="5e073-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5e073-132">System.String</span></span>

## <span data-ttu-id="5e073-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e073-133">OUTPUTS</span></span>

### <span data-ttu-id="5e073-134">Microsoft. Azure. commands. Compute. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="5e073-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="5e073-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e073-135">NOTES</span></span>

## <span data-ttu-id="5e073-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e073-136">RELATED LINKS</span></span>
