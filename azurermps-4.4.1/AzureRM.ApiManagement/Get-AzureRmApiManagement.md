---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 610f8589dbb6c01cae1a3eb37f886425a3664929
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573784"
---
# <span data-ttu-id="64ea2-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="64ea2-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="64ea2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="64ea2-103">Hämtar en lista eller en särskild beskrivning för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="64ea2-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64ea2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64ea2-104">SYNTAX</span></span>

### <span data-ttu-id="64ea2-105">Allt i abonnemanget (standard)</span><span class="sxs-lookup"><span data-stu-id="64ea2-105">All In Subscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ea2-106">Alla i resurs grupp</span><span class="sxs-lookup"><span data-stu-id="64ea2-106">All In Resource Group</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64ea2-107">Specifik API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="64ea2-107">Specific API Management Service</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64ea2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64ea2-108">DESCRIPTION</span></span>
<span data-ttu-id="64ea2-109">Cmdleten **Get-AzureRmApiManagement** hämtar en lista över alla API-hanterings tjänster under prenumeration eller angiven resurs grupp eller en särskild API-hantering.</span><span class="sxs-lookup"><span data-stu-id="64ea2-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="64ea2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64ea2-110">EXAMPLES</span></span>

### <span data-ttu-id="64ea2-111">Exempel 1: Hämta alla API-hanterings tjänster</span><span class="sxs-lookup"><span data-stu-id="64ea2-111">Example 1: Get all API Management services</span></span>
```
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="64ea2-112">Det här kommandot får alla API-hanterings tjänster inom ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="64ea2-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="64ea2-113">Exempel 2: Hämta alla API Management-tjänster med ett specifikt namn</span><span class="sxs-lookup"><span data-stu-id="64ea2-113">Example 2: Get all API Management services by a specific name</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="64ea2-114">Det här kommandot får alla API-hanterings tjänster efter namn.</span><span class="sxs-lookup"><span data-stu-id="64ea2-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="64ea2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64ea2-115">PARAMETERS</span></span>

### <span data-ttu-id="64ea2-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="64ea2-116">-Name</span></span>
<span data-ttu-id="64ea2-117">Anger namnet på API-hanteringsservern.</span><span class="sxs-lookup"><span data-stu-id="64ea2-117">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64ea2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64ea2-118">-ResourceGroupName</span></span>
<span data-ttu-id="64ea2-119">Anger namnet på den resurs grupp under vilken denna cmdlet får API Management-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="64ea2-119">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64ea2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ea2-120">-DefaultProfile</span></span>
<span data-ttu-id="64ea2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64ea2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64ea2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ea2-122">CommonParameters</span></span>
<span data-ttu-id="64ea2-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64ea2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ea2-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64ea2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ea2-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64ea2-125">INPUTS</span></span>

## <span data-ttu-id="64ea2-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64ea2-126">OUTPUTS</span></span>

### <span data-ttu-id="64ea2-127">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement]</span><span class="sxs-lookup"><span data-stu-id="64ea2-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement]</span></span>

## <span data-ttu-id="64ea2-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64ea2-128">NOTES</span></span>

## <span data-ttu-id="64ea2-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64ea2-129">RELATED LINKS</span></span>

[<span data-ttu-id="64ea2-130">Säkerhets kopiering-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="64ea2-130">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="64ea2-131">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="64ea2-131">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="64ea2-132">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="64ea2-132">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="64ea2-133">Återställ-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="64ea2-133">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


