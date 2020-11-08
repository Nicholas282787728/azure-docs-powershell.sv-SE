---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: f54998dc0d5ec8570a573870148a8cf05c265618
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089932"
---
# <span data-ttu-id="48fd7-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="48fd7-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="48fd7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="48fd7-103">Tar bort en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="48fd7-103">Removes an API Management service.</span></span>

## <span data-ttu-id="48fd7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48fd7-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48fd7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48fd7-105">DESCRIPTION</span></span>
<span data-ttu-id="48fd7-106">Cmdleten **Remove-AzApiManagement** tar bort en Azure API Management-tjänst.</span><span class="sxs-lookup"><span data-stu-id="48fd7-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="48fd7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48fd7-107">EXAMPLES</span></span>

### <span data-ttu-id="48fd7-108">Exempel 1: ta bort en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="48fd7-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="48fd7-109">Det här kommandot tar bort API-hanteringskonsolen med namnet ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="48fd7-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="48fd7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48fd7-110">PARAMETERS</span></span>

### <span data-ttu-id="48fd7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48fd7-111">-DefaultProfile</span></span>
<span data-ttu-id="48fd7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48fd7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48fd7-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="48fd7-113">-Name</span></span>
<span data-ttu-id="48fd7-114">Anger namnet på den API-hanterings distribution som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="48fd7-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="48fd7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48fd7-115">-PassThru</span></span>
<span data-ttu-id="48fd7-116">Anger att den här cmdleten returnerar ett värde för $True om åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="48fd7-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="48fd7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48fd7-117">-ResourceGroupName</span></span>
<span data-ttu-id="48fd7-118">Anger namnet på den resurs grupp som distributionen av API-hanteringen finns under.</span><span class="sxs-lookup"><span data-stu-id="48fd7-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="48fd7-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48fd7-119">-Confirm</span></span>
<span data-ttu-id="48fd7-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48fd7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48fd7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48fd7-121">-WhatIf</span></span>
<span data-ttu-id="48fd7-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="48fd7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48fd7-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="48fd7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48fd7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48fd7-124">CommonParameters</span></span>
<span data-ttu-id="48fd7-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48fd7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48fd7-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48fd7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48fd7-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48fd7-127">INPUTS</span></span>

### <span data-ttu-id="48fd7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="48fd7-128">System.String</span></span>

## <span data-ttu-id="48fd7-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48fd7-129">OUTPUTS</span></span>

### <span data-ttu-id="48fd7-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48fd7-130">System.Boolean</span></span>

## <span data-ttu-id="48fd7-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48fd7-131">NOTES</span></span>

## <span data-ttu-id="48fd7-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48fd7-132">RELATED LINKS</span></span>

[<span data-ttu-id="48fd7-133">Säkerhets kopiering-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="48fd7-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="48fd7-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="48fd7-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="48fd7-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="48fd7-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="48fd7-136">Återställ-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="48fd7-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


