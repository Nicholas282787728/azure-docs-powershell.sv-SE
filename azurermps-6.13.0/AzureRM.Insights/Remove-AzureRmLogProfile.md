---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: 92c4ea23f54025fdf32821742896459587f605f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578020"
---
# <span data-ttu-id="d058e-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="d058e-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="d058e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d058e-102">SYNOPSIS</span></span>
<span data-ttu-id="d058e-103">Tar bort en logg profil.</span><span class="sxs-lookup"><span data-stu-id="d058e-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d058e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d058e-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d058e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d058e-105">DESCRIPTION</span></span>
<span data-ttu-id="d058e-106">Cmdleten **Remove-AzureRmLogProfile** tar bort en logg profil.</span><span class="sxs-lookup"><span data-stu-id="d058e-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="d058e-107">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="d058e-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="d058e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d058e-108">EXAMPLES</span></span>

## <span data-ttu-id="d058e-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d058e-109">PARAMETERS</span></span>

### <span data-ttu-id="d058e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d058e-110">-DefaultProfile</span></span>
<span data-ttu-id="d058e-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d058e-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d058e-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="d058e-112">-Name</span></span>
<span data-ttu-id="d058e-113">Anger namnet på den logg profil som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d058e-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="d058e-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d058e-114">-PassThru</span></span>
<span data-ttu-id="d058e-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d058e-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d058e-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d058e-116">-Confirm</span></span>
<span data-ttu-id="d058e-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d058e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d058e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d058e-118">-WhatIf</span></span>
<span data-ttu-id="d058e-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d058e-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d058e-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d058e-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d058e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d058e-121">CommonParameters</span></span>
<span data-ttu-id="d058e-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d058e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d058e-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d058e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d058e-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d058e-124">INPUTS</span></span>

### <span data-ttu-id="d058e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d058e-125">System.String</span></span>

## <span data-ttu-id="d058e-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d058e-126">OUTPUTS</span></span>

### <span data-ttu-id="d058e-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d058e-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d058e-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d058e-128">NOTES</span></span>

## <span data-ttu-id="d058e-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d058e-129">RELATED LINKS</span></span>

[<span data-ttu-id="d058e-130">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="d058e-130">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="d058e-131">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="d058e-131">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

