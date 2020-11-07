---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: b7c5f713c7c245676804318b880df3f79a7ca60d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925109"
---
# <span data-ttu-id="ce459-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ce459-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="ce459-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce459-102">SYNOPSIS</span></span>
<span data-ttu-id="ce459-103">Ger åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="ce459-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="ce459-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce459-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce459-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce459-105">DESCRIPTION</span></span>
<span data-ttu-id="ce459-106">**Grant-AzDiskAccess** cmdlet ger en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="ce459-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="ce459-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce459-107">EXAMPLES</span></span>

### <span data-ttu-id="ce459-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ce459-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="ce459-109">Ge "Read"-åtkomst till disken med namnet "Disk01" i resurs gruppen med namnet "ResourceGroup01" för 60 sekunder.</span><span class="sxs-lookup"><span data-stu-id="ce459-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="ce459-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce459-110">PARAMETERS</span></span>

### <span data-ttu-id="ce459-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="ce459-111">-Access</span></span>
<span data-ttu-id="ce459-112">Anger åtkomst nivå.</span><span class="sxs-lookup"><span data-stu-id="ce459-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce459-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce459-113">-AsJob</span></span>
<span data-ttu-id="ce459-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ce459-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce459-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce459-115">-DefaultProfile</span></span>
<span data-ttu-id="ce459-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce459-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce459-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ce459-117">-DiskName</span></span>
<span data-ttu-id="ce459-118">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="ce459-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="ce459-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="ce459-119">-DurationInSecond</span></span>
<span data-ttu-id="ce459-120">Anger åtkomst längd i sekunder.</span><span class="sxs-lookup"><span data-stu-id="ce459-120">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce459-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce459-121">-ResourceGroupName</span></span>
<span data-ttu-id="ce459-122">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ce459-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ce459-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce459-123">-Confirm</span></span>
<span data-ttu-id="ce459-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce459-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce459-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce459-125">-WhatIf</span></span>
<span data-ttu-id="ce459-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce459-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce459-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce459-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce459-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce459-128">CommonParameters</span></span>
<span data-ttu-id="ce459-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce459-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce459-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce459-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce459-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce459-131">INPUTS</span></span>

### <span data-ttu-id="ce459-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ce459-132">System.String</span></span>

## <span data-ttu-id="ce459-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce459-133">OUTPUTS</span></span>

### <span data-ttu-id="ce459-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="ce459-134">System.Object</span></span>

## <span data-ttu-id="ce459-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce459-135">NOTES</span></span>

## <span data-ttu-id="ce459-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce459-136">RELATED LINKS</span></span>

