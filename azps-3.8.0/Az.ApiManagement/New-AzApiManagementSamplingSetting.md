---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 61f046576c14b61a59b55c52dd69c3e72b2c839e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089943"
---
# <span data-ttu-id="99db1-101">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="99db1-101">New-AzApiManagementSamplingSetting</span></span>

## <span data-ttu-id="99db1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99db1-102">SYNOPSIS</span></span>
<span data-ttu-id="99db1-103">Skapa en ny samplings inställning för diagnostiken</span><span class="sxs-lookup"><span data-stu-id="99db1-103">Create a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="99db1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99db1-104">SYNTAX</span></span>

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99db1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99db1-105">DESCRIPTION</span></span>
<span data-ttu-id="99db1-106">Cmdlet **New-AzApiManagementSamplingSetting** skapar en ny samplings inställning för diagnostiken</span><span class="sxs-lookup"><span data-stu-id="99db1-106">The cmdlet **New-AzApiManagementSamplingSetting** creates a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="99db1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99db1-107">EXAMPLES</span></span>

### <span data-ttu-id="99db1-108">Exempel 1: skapa en grundläggande exempel inställning</span><span class="sxs-lookup"><span data-stu-id="99db1-108">Example 1 : Create a basic Sampling setting</span></span>
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

<span data-ttu-id="99db1-109">Skapar en samplings inställning av `Fixed` typen med loggning för 100% av begäran/svar</span><span class="sxs-lookup"><span data-stu-id="99db1-109">Creates a sampling setting of `Fixed` type with logging for 100% of the requests / responses</span></span>

## <span data-ttu-id="99db1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99db1-110">PARAMETERS</span></span>

### <span data-ttu-id="99db1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99db1-111">-DefaultProfile</span></span>
<span data-ttu-id="99db1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99db1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99db1-113">-SamplingPercentage</span><span class="sxs-lookup"><span data-stu-id="99db1-113">-SamplingPercentage</span></span>
<span data-ttu-id="99db1-114">Satsen för provtagning för fast taxa.</span><span class="sxs-lookup"><span data-stu-id="99db1-114">Rate of Sampling for Fixed Rate Sampling.</span></span> <span data-ttu-id="99db1-115">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="99db1-115">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99db1-116">-SamplingType</span><span class="sxs-lookup"><span data-stu-id="99db1-116">-SamplingType</span></span>
<span data-ttu-id="99db1-117">Typ av sampling.</span><span class="sxs-lookup"><span data-stu-id="99db1-117">The Type of Sampling.</span></span>
<span data-ttu-id="99db1-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="99db1-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99db1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99db1-119">CommonParameters</span></span>
<span data-ttu-id="99db1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99db1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99db1-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99db1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99db1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99db1-122">INPUTS</span></span>

### <span data-ttu-id="99db1-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="99db1-123">None</span></span>

## <span data-ttu-id="99db1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99db1-124">OUTPUTS</span></span>

### <span data-ttu-id="99db1-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="99db1-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

## <span data-ttu-id="99db1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99db1-126">NOTES</span></span>

## <span data-ttu-id="99db1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99db1-127">RELATED LINKS</span></span>

[<span data-ttu-id="99db1-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="99db1-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="99db1-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="99db1-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="99db1-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="99db1-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="99db1-131">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="99db1-131">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
