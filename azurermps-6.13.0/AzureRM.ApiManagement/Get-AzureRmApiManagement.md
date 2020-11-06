---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: bff36b7bcb37dd099f9aa50a99bed9538111e8d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582867"
---
# <span data-ttu-id="c73cb-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c73cb-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="c73cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c73cb-102">SYNOPSIS</span></span>
<span data-ttu-id="c73cb-103">Hämtar en lista eller en särskild beskrivning för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c73cb-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c73cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c73cb-104">SYNTAX</span></span>

### <span data-ttu-id="c73cb-105">GetBySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="c73cb-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c73cb-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c73cb-106">GetByResourceGroup</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c73cb-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="c73cb-107">GetByResource</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c73cb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c73cb-108">DESCRIPTION</span></span>
<span data-ttu-id="c73cb-109">Cmdleten **Get-AzureRmApiManagement** hämtar en lista över alla API-hanterings tjänster under prenumeration eller angiven resurs grupp eller en särskild API-hantering.</span><span class="sxs-lookup"><span data-stu-id="c73cb-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="c73cb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c73cb-110">EXAMPLES</span></span>

### <span data-ttu-id="c73cb-111">Exempel 1: Hämta alla API-hanterings tjänster</span><span class="sxs-lookup"><span data-stu-id="c73cb-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="c73cb-112">Det här kommandot får alla API-hanterings tjänster inom ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="c73cb-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="c73cb-113">Exempel 2: Hämta alla API Management-tjänster med ett specifikt namn</span><span class="sxs-lookup"><span data-stu-id="c73cb-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="c73cb-114">Det här kommandot får alla API-hanterings tjänster efter namn.</span><span class="sxs-lookup"><span data-stu-id="c73cb-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="c73cb-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c73cb-115">PARAMETERS</span></span>

### <span data-ttu-id="c73cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c73cb-116">-DefaultProfile</span></span>
<span data-ttu-id="c73cb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c73cb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c73cb-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c73cb-118">-Name</span></span>
<span data-ttu-id="c73cb-119">Anger namnet på API-hanteringsservern.</span><span class="sxs-lookup"><span data-stu-id="c73cb-119">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="c73cb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c73cb-120">-ResourceGroupName</span></span>
<span data-ttu-id="c73cb-121">Anger namnet på den resurs grupp under vilken denna cmdlet får API Management-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c73cb-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="c73cb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c73cb-122">CommonParameters</span></span>
<span data-ttu-id="c73cb-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c73cb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c73cb-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c73cb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c73cb-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c73cb-125">INPUTS</span></span>

### <span data-ttu-id="c73cb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c73cb-126">System.String</span></span>

## <span data-ttu-id="c73cb-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c73cb-127">OUTPUTS</span></span>

### <span data-ttu-id="c73cb-128">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c73cb-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c73cb-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c73cb-129">NOTES</span></span>

## <span data-ttu-id="c73cb-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c73cb-130">RELATED LINKS</span></span>

[<span data-ttu-id="c73cb-131">Säkerhets kopiering-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c73cb-131">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="c73cb-132">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c73cb-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="c73cb-133">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c73cb-133">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="c73cb-134">Återställ-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c73cb-134">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


