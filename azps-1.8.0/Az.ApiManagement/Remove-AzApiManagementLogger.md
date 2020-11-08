---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: d5f04c44638f5aa0cfc34ca528d57fca8afe5b08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917774"
---
# <span data-ttu-id="9e408-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9e408-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="9e408-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e408-102">SYNOPSIS</span></span>
<span data-ttu-id="9e408-103">Tar bort en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="9e408-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="9e408-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e408-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e408-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e408-105">DESCRIPTION</span></span>
<span data-ttu-id="9e408-106">Cmdleten **Remove-AzApiManagementLogger** tar bort en Azure API Management- **loggning**.</span><span class="sxs-lookup"><span data-stu-id="9e408-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="9e408-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e408-107">EXAMPLES</span></span>

### <span data-ttu-id="9e408-108">Exempel 1: ta bort en loggare</span><span class="sxs-lookup"><span data-stu-id="9e408-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="9e408-109">Det här kommandot tar bort en loggare som har ID-Logger123.</span><span class="sxs-lookup"><span data-stu-id="9e408-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="9e408-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e408-110">PARAMETERS</span></span>

### <span data-ttu-id="9e408-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="9e408-111">-Context</span></span>
<span data-ttu-id="9e408-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9e408-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e408-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e408-113">-DefaultProfile</span></span>
<span data-ttu-id="9e408-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e408-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e408-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="9e408-115">-LoggerId</span></span>
<span data-ttu-id="9e408-116">Anger ID för den logg som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9e408-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="9e408-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e408-117">-PassThru</span></span>
<span data-ttu-id="9e408-118">Anger att denna cmdlet returnerar ett värde för $True om åtgärden lyckas eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="9e408-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="9e408-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e408-119">-Confirm</span></span>
<span data-ttu-id="9e408-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e408-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e408-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e408-121">-WhatIf</span></span>
<span data-ttu-id="9e408-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e408-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e408-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e408-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e408-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e408-124">CommonParameters</span></span>
<span data-ttu-id="9e408-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e408-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e408-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e408-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e408-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e408-127">INPUTS</span></span>

### <span data-ttu-id="9e408-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9e408-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e408-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9e408-129">System.String</span></span>

### <span data-ttu-id="9e408-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9e408-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9e408-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e408-131">OUTPUTS</span></span>

### <span data-ttu-id="9e408-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e408-132">System.Boolean</span></span>

## <span data-ttu-id="9e408-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e408-133">NOTES</span></span>

## <span data-ttu-id="9e408-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e408-134">RELATED LINKS</span></span>

[<span data-ttu-id="9e408-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9e408-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="9e408-136">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9e408-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="9e408-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9e408-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)

