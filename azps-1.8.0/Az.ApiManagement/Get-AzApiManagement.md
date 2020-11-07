---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: c636da952c02b4f2b4795cd1703c276a23a8221c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743428"
---
# <span data-ttu-id="99b1e-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="99b1e-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="99b1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="99b1e-103">Hämtar en lista eller en särskild beskrivning för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="99b1e-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="99b1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99b1e-104">SYNTAX</span></span>

### <span data-ttu-id="99b1e-105">GetBySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="99b1e-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b1e-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99b1e-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b1e-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="99b1e-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99b1e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99b1e-108">DESCRIPTION</span></span>
<span data-ttu-id="99b1e-109">Cmdleten **Get-AzApiManagement** hämtar en lista över alla API-hanterings tjänster under prenumeration eller angiven resurs grupp eller en särskild API-hantering.</span><span class="sxs-lookup"><span data-stu-id="99b1e-109">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="99b1e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99b1e-110">EXAMPLES</span></span>

### <span data-ttu-id="99b1e-111">Exempel 1: Hämta alla API-hanterings tjänster</span><span class="sxs-lookup"><span data-stu-id="99b1e-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="99b1e-112">Det här kommandot får alla API-hanterings tjänster inom ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="99b1e-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="99b1e-113">Exempel 2: Hämta alla API Management-tjänster med ett specifikt namn</span><span class="sxs-lookup"><span data-stu-id="99b1e-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="99b1e-114">Det här kommandot får alla API-hanterings tjänster efter namn.</span><span class="sxs-lookup"><span data-stu-id="99b1e-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="99b1e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99b1e-115">PARAMETERS</span></span>

### <span data-ttu-id="99b1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b1e-116">-DefaultProfile</span></span>
<span data-ttu-id="99b1e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99b1e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99b1e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="99b1e-118">-Name</span></span>
<span data-ttu-id="99b1e-119">Anger namnet på API-hanteringsservern.</span><span class="sxs-lookup"><span data-stu-id="99b1e-119">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b1e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b1e-120">-ResourceGroupName</span></span>
<span data-ttu-id="99b1e-121">Anger namnet på den resurs grupp under vilken denna cmdlet får API Management-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="99b1e-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b1e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b1e-122">CommonParameters</span></span>
<span data-ttu-id="99b1e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99b1e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b1e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99b1e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b1e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99b1e-125">INPUTS</span></span>

### <span data-ttu-id="99b1e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="99b1e-126">System.String</span></span>

## <span data-ttu-id="99b1e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99b1e-127">OUTPUTS</span></span>

### <span data-ttu-id="99b1e-128">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="99b1e-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="99b1e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99b1e-129">NOTES</span></span>

## <span data-ttu-id="99b1e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99b1e-130">RELATED LINKS</span></span>

[<span data-ttu-id="99b1e-131">Säkerhets kopiering-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="99b1e-131">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="99b1e-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="99b1e-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="99b1e-133">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="99b1e-133">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="99b1e-134">Återställ-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="99b1e-134">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


