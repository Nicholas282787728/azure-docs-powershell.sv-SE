---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 58cbbfd2314589fd6b28f2ff375aa268c39e63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573685"
---
# <span data-ttu-id="8aaac-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8aaac-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="8aaac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8aaac-102">SYNOPSIS</span></span>
<span data-ttu-id="8aaac-103">Återkallar en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="8aaac-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8aaac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8aaac-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aaac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8aaac-105">DESCRIPTION</span></span>
<span data-ttu-id="8aaac-106">Cmdleten **REVOKE-AzureRmDiskAccess** avvisar en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="8aaac-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="8aaac-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8aaac-107">EXAMPLES</span></span>

### <span data-ttu-id="8aaac-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8aaac-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="8aaac-109">Återkalla åtkomsten till disken "Disk01" i resurs gruppen med namnet "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="8aaac-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="8aaac-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8aaac-110">PARAMETERS</span></span>

### <span data-ttu-id="8aaac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aaac-111">-DefaultProfile</span></span>
<span data-ttu-id="8aaac-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8aaac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8aaac-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="8aaac-113">-DiskName</span></span>
<span data-ttu-id="8aaac-114">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="8aaac-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="8aaac-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aaac-115">-ResourceGroupName</span></span>
<span data-ttu-id="8aaac-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8aaac-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8aaac-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8aaac-117">-Confirm</span></span>
<span data-ttu-id="8aaac-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8aaac-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aaac-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aaac-119">-WhatIf</span></span>
<span data-ttu-id="8aaac-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8aaac-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8aaac-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8aaac-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aaac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aaac-122">CommonParameters</span></span>
<span data-ttu-id="8aaac-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aaac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aaac-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8aaac-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aaac-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8aaac-125">INPUTS</span></span>

### <span data-ttu-id="8aaac-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8aaac-126">System.String</span></span>

## <span data-ttu-id="8aaac-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8aaac-127">OUTPUTS</span></span>

### <span data-ttu-id="8aaac-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="8aaac-128">System.Object</span></span>

## <span data-ttu-id="8aaac-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8aaac-129">NOTES</span></span>

## <span data-ttu-id="8aaac-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8aaac-130">RELATED LINKS</span></span>

