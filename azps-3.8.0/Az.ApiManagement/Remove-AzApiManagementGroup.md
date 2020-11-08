---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 73e1fbee1dd20a9a30260727f693376346c87f0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089881"
---
# <span data-ttu-id="78693-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="78693-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="78693-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78693-102">SYNOPSIS</span></span>
<span data-ttu-id="78693-103">Tar bort en befintlig API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="78693-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="78693-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78693-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78693-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78693-105">DESCRIPTION</span></span>
<span data-ttu-id="78693-106">Cmdleten **Remove-AzApiManagementGroup** tar bort en befintlig API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="78693-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="78693-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78693-107">EXAMPLES</span></span>

### <span data-ttu-id="78693-108">Exempel 1: ta bort en befintlig hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="78693-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="78693-109">Det här kommandot tar bort en befintlig hanterings grupp med namnet Group0001 och ber inte användaren att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="78693-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="78693-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78693-110">PARAMETERS</span></span>

### <span data-ttu-id="78693-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="78693-111">-Context</span></span>
<span data-ttu-id="78693-112">Anger förekomsten av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="78693-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78693-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78693-113">-DefaultProfile</span></span>
<span data-ttu-id="78693-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78693-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78693-115">-Kund-</span><span class="sxs-lookup"><span data-stu-id="78693-115">-GroupId</span></span>
<span data-ttu-id="78693-116">Anger ID: till en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="78693-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="78693-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78693-117">-PassThru</span></span>
<span data-ttu-id="78693-118">Anger att denna cmdlet returnerar ett värde för $True om det lyckas, eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="78693-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78693-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78693-119">-Confirm</span></span>
<span data-ttu-id="78693-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78693-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78693-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78693-121">-WhatIf</span></span>
<span data-ttu-id="78693-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78693-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78693-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78693-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78693-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78693-124">CommonParameters</span></span>
<span data-ttu-id="78693-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78693-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78693-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78693-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78693-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78693-127">INPUTS</span></span>

### <span data-ttu-id="78693-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="78693-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="78693-129">System. String</span><span class="sxs-lookup"><span data-stu-id="78693-129">System.String</span></span>

### <span data-ttu-id="78693-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="78693-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="78693-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78693-131">OUTPUTS</span></span>

### <span data-ttu-id="78693-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78693-132">System.Boolean</span></span>

## <span data-ttu-id="78693-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78693-133">NOTES</span></span>

## <span data-ttu-id="78693-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78693-134">RELATED LINKS</span></span>

[<span data-ttu-id="78693-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="78693-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="78693-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="78693-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="78693-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="78693-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


