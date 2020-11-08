---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 76fb2e7483bb510d5eceb92b51f7e5e538c3b22b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089825"
---
# <span data-ttu-id="eba6b-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="eba6b-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="eba6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eba6b-102">SYNOPSIS</span></span>
<span data-ttu-id="eba6b-103">Återkallar en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="eba6b-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="eba6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eba6b-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eba6b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eba6b-105">DESCRIPTION</span></span>
<span data-ttu-id="eba6b-106">Cmdleten **REVOKE-AzDiskAccess** avvisar en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="eba6b-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="eba6b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eba6b-107">EXAMPLES</span></span>

### <span data-ttu-id="eba6b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eba6b-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="eba6b-109">Återkalla åtkomsten till disken "Disk01" i resurs gruppen med namnet "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="eba6b-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="eba6b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eba6b-110">PARAMETERS</span></span>

### <span data-ttu-id="eba6b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eba6b-111">-AsJob</span></span>
<span data-ttu-id="eba6b-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="eba6b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eba6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba6b-113">-DefaultProfile</span></span>
<span data-ttu-id="eba6b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eba6b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eba6b-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="eba6b-115">-DiskName</span></span>
<span data-ttu-id="eba6b-116">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="eba6b-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="eba6b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eba6b-117">-ResourceGroupName</span></span>
<span data-ttu-id="eba6b-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="eba6b-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eba6b-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eba6b-119">-Confirm</span></span>
<span data-ttu-id="eba6b-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eba6b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eba6b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eba6b-121">-WhatIf</span></span>
<span data-ttu-id="eba6b-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eba6b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eba6b-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eba6b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eba6b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba6b-124">CommonParameters</span></span>
<span data-ttu-id="eba6b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba6b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba6b-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eba6b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba6b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eba6b-127">INPUTS</span></span>

### <span data-ttu-id="eba6b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eba6b-128">System.String</span></span>

## <span data-ttu-id="eba6b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eba6b-129">OUTPUTS</span></span>

### <span data-ttu-id="eba6b-130">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="eba6b-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="eba6b-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eba6b-131">NOTES</span></span>

## <span data-ttu-id="eba6b-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eba6b-132">RELATED LINKS</span></span>
