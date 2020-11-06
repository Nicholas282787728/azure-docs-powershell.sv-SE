---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 3c36d0b21b1fdda1282a1184f90728e827515195
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575050"
---
# <span data-ttu-id="fada8-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fada8-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="fada8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fada8-102">SYNOPSIS</span></span>
<span data-ttu-id="fada8-103">Tar bort en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="fada8-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fada8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fada8-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fada8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fada8-105">DESCRIPTION</span></span>
<span data-ttu-id="fada8-106">Cmdleten **Remove-AzureRmApiManagementLogger** tar bort en Azure API Management- **loggning**.</span><span class="sxs-lookup"><span data-stu-id="fada8-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="fada8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fada8-107">EXAMPLES</span></span>

### <span data-ttu-id="fada8-108">Exempel 1: ta bort en loggare</span><span class="sxs-lookup"><span data-stu-id="fada8-108">Example 1: Remove a logger</span></span>
```
PS C:\>Remove-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="fada8-109">Det här kommandot tar bort en loggare som har ID-Logger123.</span><span class="sxs-lookup"><span data-stu-id="fada8-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="fada8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fada8-110">PARAMETERS</span></span>

### <span data-ttu-id="fada8-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="fada8-111">-Context</span></span>
<span data-ttu-id="fada8-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fada8-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fada8-113">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="fada8-113">-LoggerId</span></span>
<span data-ttu-id="fada8-114">Anger ID för den logg som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="fada8-114">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="fada8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fada8-115">-PassThru</span></span>
<span data-ttu-id="fada8-116">Anger att denna cmdlet returnerar ett värde för $True om åtgärden lyckas eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="fada8-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="fada8-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fada8-117">-Confirm</span></span>
<span data-ttu-id="fada8-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fada8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fada8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fada8-119">-WhatIf</span></span>
<span data-ttu-id="fada8-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fada8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fada8-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fada8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fada8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fada8-122">-DefaultProfile</span></span>
<span data-ttu-id="fada8-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fada8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fada8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fada8-124">CommonParameters</span></span>
<span data-ttu-id="fada8-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fada8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fada8-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fada8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fada8-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fada8-127">INPUTS</span></span>

## <span data-ttu-id="fada8-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fada8-128">OUTPUTS</span></span>

### <span data-ttu-id="fada8-129">Returtyp</span><span class="sxs-lookup"><span data-stu-id="fada8-129">Boolean</span></span>

## <span data-ttu-id="fada8-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fada8-130">NOTES</span></span>

## <span data-ttu-id="fada8-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fada8-131">RELATED LINKS</span></span>

[<span data-ttu-id="fada8-132">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fada8-132">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="fada8-133">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fada8-133">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="fada8-134">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="fada8-134">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


