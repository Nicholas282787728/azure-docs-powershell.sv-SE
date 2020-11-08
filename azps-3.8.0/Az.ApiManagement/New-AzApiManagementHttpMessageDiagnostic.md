---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: d3706168a23a32d4338069cb593ef8dd71242896
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089966"
---
# <span data-ttu-id="c5284-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c5284-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="c5284-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5284-102">SYNOPSIS</span></span>
<span data-ttu-id="c5284-103">Skapar en instans av **PsApiManagementHttpMessageDiagnostic** som är en diagnostisk inställning för HTTP-meddelanden</span><span class="sxs-lookup"><span data-stu-id="c5284-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="c5284-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5284-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5284-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5284-105">DESCRIPTION</span></span>
<span data-ttu-id="c5284-106">Cmdlet **New-AzApiManagementHttpMessageDiagnostic** skapar en inställning för HTTP-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="c5284-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="c5284-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5284-107">EXAMPLES</span></span>

### <span data-ttu-id="c5284-108">Exempel 1: skapa en grundläggande inställning för HTTP-meddelanden</span><span class="sxs-lookup"><span data-stu-id="c5284-108">Example 1 : Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="c5284-109">Skapa en http-meddelandekö för loggning `Content-Type` och `User-Agent` rubriker tillsammans med 100 byte `body`</span><span class="sxs-lookup"><span data-stu-id="c5284-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="c5284-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5284-110">PARAMETERS</span></span>

### <span data-ttu-id="c5284-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="c5284-111">-BodyBytesToLog</span></span>
<span data-ttu-id="c5284-112">Antal byte för begäran om att logga.</span><span class="sxs-lookup"><span data-stu-id="c5284-112">Number of request body bytes to log.</span></span> <span data-ttu-id="c5284-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c5284-113">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5284-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5284-114">-DefaultProfile</span></span>
<span data-ttu-id="c5284-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c5284-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5284-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="c5284-116">-HeadersToLog</span></span>
<span data-ttu-id="c5284-117">Matrisen med rubriker att logga.</span><span class="sxs-lookup"><span data-stu-id="c5284-117">The array of headers to log.</span></span> <span data-ttu-id="c5284-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c5284-118">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5284-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5284-119">CommonParameters</span></span>
<span data-ttu-id="c5284-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5284-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5284-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5284-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5284-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5284-122">INPUTS</span></span>

### <span data-ttu-id="c5284-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="c5284-123">None</span></span>

## <span data-ttu-id="c5284-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5284-124">OUTPUTS</span></span>

### <span data-ttu-id="c5284-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c5284-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="c5284-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5284-126">NOTES</span></span>

## <span data-ttu-id="c5284-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5284-127">RELATED LINKS</span></span>

[<span data-ttu-id="c5284-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c5284-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c5284-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c5284-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)