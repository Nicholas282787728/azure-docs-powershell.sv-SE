---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 5a46e75f7ce7b0639de015de975c321c9d5c1ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573772"
---
# <span data-ttu-id="65a17-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="65a17-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="65a17-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65a17-102">SYNOPSIS</span></span>
<span data-ttu-id="65a17-103">Tar bort en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="65a17-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65a17-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65a17-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65a17-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65a17-105">DESCRIPTION</span></span>
<span data-ttu-id="65a17-106">Cmdleten **Remove-AzureRmApiManagement** tar bort en Azure API Management-tjänst.</span><span class="sxs-lookup"><span data-stu-id="65a17-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="65a17-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65a17-107">EXAMPLES</span></span>

### <span data-ttu-id="65a17-108">Exempel 1: ta bort en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="65a17-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="65a17-109">Det här kommandot tar bort API-hanteringskonsolen med namnet ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="65a17-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="65a17-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65a17-110">PARAMETERS</span></span>

### <span data-ttu-id="65a17-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="65a17-111">-Name</span></span>
<span data-ttu-id="65a17-112">Anger namnet på den API-hanterings distribution som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="65a17-112">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="65a17-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65a17-113">-PassThru</span></span>
<span data-ttu-id="65a17-114">Anger att den här cmdleten returnerar ett värde för $True om åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="65a17-114">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="65a17-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65a17-115">-ResourceGroupName</span></span>
<span data-ttu-id="65a17-116">Anger namnet på den resurs grupp som distributionen av API-hanteringen finns under.</span><span class="sxs-lookup"><span data-stu-id="65a17-116">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="65a17-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="65a17-117">-Confirm</span></span>
<span data-ttu-id="65a17-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65a17-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a17-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65a17-119">-WhatIf</span></span>
<span data-ttu-id="65a17-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="65a17-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65a17-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="65a17-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a17-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a17-122">-DefaultProfile</span></span>
<span data-ttu-id="65a17-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65a17-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65a17-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a17-124">CommonParameters</span></span>
<span data-ttu-id="65a17-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a17-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a17-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65a17-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a17-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65a17-127">INPUTS</span></span>

## <span data-ttu-id="65a17-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65a17-128">OUTPUTS</span></span>

### <span data-ttu-id="65a17-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65a17-129">System.Boolean</span></span>

## <span data-ttu-id="65a17-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65a17-130">NOTES</span></span>

## <span data-ttu-id="65a17-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65a17-131">RELATED LINKS</span></span>

[<span data-ttu-id="65a17-132">Säkerhets kopiering-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="65a17-132">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="65a17-133">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="65a17-133">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="65a17-134">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="65a17-134">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="65a17-135">Återställ-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="65a17-135">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)

