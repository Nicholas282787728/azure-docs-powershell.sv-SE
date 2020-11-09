---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323921"
---
# <span data-ttu-id="8a9db-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8a9db-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="8a9db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a9db-102">SYNOPSIS</span></span>
<span data-ttu-id="8a9db-103">Skapar en disk åtkomst resurs</span><span class="sxs-lookup"><span data-stu-id="8a9db-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="8a9db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a9db-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a9db-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a9db-105">DESCRIPTION</span></span>
<span data-ttu-id="8a9db-106">Cmdleten **New-AzDiskAccess** skapar en disk åtkomst resurs</span><span class="sxs-lookup"><span data-stu-id="8a9db-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="8a9db-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a9db-107">EXAMPLES</span></span>

### <span data-ttu-id="8a9db-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8a9db-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="8a9db-109">Det här kommandot skapar en disk åtkomst med angivna egenskaper.</span><span class="sxs-lookup"><span data-stu-id="8a9db-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="8a9db-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a9db-110">PARAMETERS</span></span>

### <span data-ttu-id="8a9db-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a9db-111">-AsJob</span></span>
<span data-ttu-id="8a9db-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8a9db-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a9db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a9db-113">-DefaultProfile</span></span>
<span data-ttu-id="8a9db-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a9db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a9db-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="8a9db-115">-Location</span></span>
<span data-ttu-id="8a9db-116">Anger platsen.</span><span class="sxs-lookup"><span data-stu-id="8a9db-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9db-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a9db-117">-Name</span></span>
<span data-ttu-id="8a9db-118">Anger namnet på en disk åtkomst.</span><span class="sxs-lookup"><span data-stu-id="8a9db-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a9db-119">-ResourceGroupName</span></span>
<span data-ttu-id="8a9db-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8a9db-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8a9db-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a9db-121">-Confirm</span></span>
<span data-ttu-id="8a9db-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a9db-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a9db-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a9db-123">-WhatIf</span></span>
<span data-ttu-id="8a9db-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a9db-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a9db-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a9db-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a9db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a9db-126">CommonParameters</span></span>
<span data-ttu-id="8a9db-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a9db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a9db-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a9db-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a9db-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a9db-129">INPUTS</span></span>

### <span data-ttu-id="8a9db-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8a9db-130">System.String</span></span>

## <span data-ttu-id="8a9db-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a9db-131">OUTPUTS</span></span>

### <span data-ttu-id="8a9db-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8a9db-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="8a9db-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a9db-133">NOTES</span></span>

## <span data-ttu-id="8a9db-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a9db-134">RELATED LINKS</span></span>
