---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: a1b06a870822f2fef0bf2f9a39321c13642f8cad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586219"
---
# <span data-ttu-id="aacb8-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="aacb8-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="aacb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aacb8-102">SYNOPSIS</span></span>
<span data-ttu-id="aacb8-103">Ger åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="aacb8-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aacb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aacb8-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aacb8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aacb8-105">DESCRIPTION</span></span>
<span data-ttu-id="aacb8-106">**Grant-AzureRmDiskAccess** cmdlet ger en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="aacb8-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="aacb8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aacb8-107">EXAMPLES</span></span>

### <span data-ttu-id="aacb8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="aacb8-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="aacb8-109">Ge "Read"-åtkomst till disken med namnet "Disk01" i resurs gruppen med namnet "ResourceGroup01" för 60 sekunder.</span><span class="sxs-lookup"><span data-stu-id="aacb8-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="aacb8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aacb8-110">PARAMETERS</span></span>

### <span data-ttu-id="aacb8-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="aacb8-111">-Access</span></span>
<span data-ttu-id="aacb8-112">Anger åtkomst nivå.</span><span class="sxs-lookup"><span data-stu-id="aacb8-112">Specifies Access level.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aacb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aacb8-113">-DefaultProfile</span></span>
<span data-ttu-id="aacb8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aacb8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aacb8-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="aacb8-115">-DiskName</span></span>
<span data-ttu-id="aacb8-116">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="aacb8-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="aacb8-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="aacb8-117">-DurationInSecond</span></span>
<span data-ttu-id="aacb8-118">Anger åtkomst längd i sekunder.</span><span class="sxs-lookup"><span data-stu-id="aacb8-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aacb8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aacb8-119">-ResourceGroupName</span></span>
<span data-ttu-id="aacb8-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="aacb8-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="aacb8-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aacb8-121">-Confirm</span></span>
<span data-ttu-id="aacb8-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aacb8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aacb8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aacb8-123">-WhatIf</span></span>
<span data-ttu-id="aacb8-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aacb8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aacb8-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aacb8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aacb8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aacb8-126">CommonParameters</span></span>
<span data-ttu-id="aacb8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aacb8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aacb8-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aacb8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aacb8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aacb8-129">INPUTS</span></span>

### <span data-ttu-id="aacb8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="aacb8-130">System.String</span></span>

## <span data-ttu-id="aacb8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aacb8-131">OUTPUTS</span></span>

### <span data-ttu-id="aacb8-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="aacb8-132">System.Object</span></span>

## <span data-ttu-id="aacb8-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aacb8-133">NOTES</span></span>

## <span data-ttu-id="aacb8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aacb8-134">RELATED LINKS</span></span>

