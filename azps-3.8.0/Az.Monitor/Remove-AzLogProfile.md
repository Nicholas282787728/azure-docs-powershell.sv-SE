---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
ms.openlocfilehash: 3c8dda7d7b84ae4ee7017c88e211b2ab5db46360
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925689"
---
# <span data-ttu-id="27b12-101">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="27b12-101">Remove-AzLogProfile</span></span>

## <span data-ttu-id="27b12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27b12-102">SYNOPSIS</span></span>
<span data-ttu-id="27b12-103">Tar bort en logg profil.</span><span class="sxs-lookup"><span data-stu-id="27b12-103">Removes a log profile.</span></span>

## <span data-ttu-id="27b12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27b12-104">SYNTAX</span></span>

```
Remove-AzLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27b12-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27b12-105">DESCRIPTION</span></span>
<span data-ttu-id="27b12-106">Cmdleten **Remove-AzLogProfile** tar bort en logg profil.</span><span class="sxs-lookup"><span data-stu-id="27b12-106">The **Remove-AzLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="27b12-107">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="27b12-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="27b12-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27b12-108">EXAMPLES</span></span>

## <span data-ttu-id="27b12-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27b12-109">PARAMETERS</span></span>

### <span data-ttu-id="27b12-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b12-110">-DefaultProfile</span></span>
<span data-ttu-id="27b12-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="27b12-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27b12-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="27b12-112">-Name</span></span>
<span data-ttu-id="27b12-113">Anger namnet på den logg profil som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="27b12-113">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b12-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27b12-114">-PassThru</span></span>
<span data-ttu-id="27b12-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="27b12-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="27b12-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="27b12-116">-Confirm</span></span>
<span data-ttu-id="27b12-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27b12-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27b12-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b12-118">-WhatIf</span></span>
<span data-ttu-id="27b12-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="27b12-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27b12-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="27b12-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27b12-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b12-121">CommonParameters</span></span>
<span data-ttu-id="27b12-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27b12-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b12-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27b12-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b12-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27b12-124">INPUTS</span></span>

### <span data-ttu-id="27b12-125">System. String</span><span class="sxs-lookup"><span data-stu-id="27b12-125">System.String</span></span>

## <span data-ttu-id="27b12-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27b12-126">OUTPUTS</span></span>

### <span data-ttu-id="27b12-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="27b12-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="27b12-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27b12-128">NOTES</span></span>

## <span data-ttu-id="27b12-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27b12-129">RELATED LINKS</span></span>

[<span data-ttu-id="27b12-130">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="27b12-130">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="27b12-131">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="27b12-131">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

