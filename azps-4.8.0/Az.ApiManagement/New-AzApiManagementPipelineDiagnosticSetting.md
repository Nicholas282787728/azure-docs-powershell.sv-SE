---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103351"
---
# <span data-ttu-id="cfe97-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="cfe97-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="cfe97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfe97-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe97-103">Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="cfe97-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="cfe97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfe97-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfe97-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfe97-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe97-106">Cmdlet **New-AzApiManagementPipelineDiagnosticSetting** skapar diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="cfe97-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="cfe97-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfe97-107">EXAMPLES</span></span>

### <span data-ttu-id="cfe97-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cfe97-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="cfe97-109">Skapa en pipeline-diagnostik som ska användas i antingen klient delen eller Server delen i den diagnostiska enheten.</span><span class="sxs-lookup"><span data-stu-id="cfe97-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="cfe97-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfe97-110">PARAMETERS</span></span>

### <span data-ttu-id="cfe97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe97-111">-DefaultProfile</span></span>
<span data-ttu-id="cfe97-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe97-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfe97-113">-Begäran</span><span class="sxs-lookup"><span data-stu-id="cfe97-113">-Request</span></span>
<span data-ttu-id="cfe97-114">Diagnostisk inställning för begäran.</span><span class="sxs-lookup"><span data-stu-id="cfe97-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="cfe97-115">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="cfe97-115">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe97-116">-Svar</span><span class="sxs-lookup"><span data-stu-id="cfe97-116">-Response</span></span>
<span data-ttu-id="cfe97-117">Diagnostisk inställning för svar.</span><span class="sxs-lookup"><span data-stu-id="cfe97-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="cfe97-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="cfe97-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe97-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe97-119">CommonParameters</span></span>
<span data-ttu-id="cfe97-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe97-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe97-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfe97-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe97-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfe97-122">INPUTS</span></span>

### <span data-ttu-id="cfe97-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="cfe97-123">None</span></span>

## <span data-ttu-id="cfe97-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfe97-124">OUTPUTS</span></span>

### <span data-ttu-id="cfe97-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="cfe97-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="cfe97-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfe97-126">NOTES</span></span>

## <span data-ttu-id="cfe97-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfe97-127">RELATED LINKS</span></span>

[<span data-ttu-id="cfe97-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cfe97-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="cfe97-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cfe97-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="cfe97-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cfe97-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="cfe97-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cfe97-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

