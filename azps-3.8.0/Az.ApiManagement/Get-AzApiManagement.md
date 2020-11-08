---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089683"
---
# <span data-ttu-id="50957-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="50957-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="50957-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50957-102">SYNOPSIS</span></span>
<span data-ttu-id="50957-103">Hämtar en lista eller en särskild beskrivning för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="50957-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="50957-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50957-104">SYNTAX</span></span>

### <span data-ttu-id="50957-105">GetBySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="50957-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50957-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50957-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50957-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="50957-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50957-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="50957-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50957-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50957-109">DESCRIPTION</span></span>
<span data-ttu-id="50957-110">Cmdleten **Get-AzApiManagement** hämtar en lista över alla API-hanterings tjänster under prenumeration eller angiven resurs grupp eller en särskild API-hantering.</span><span class="sxs-lookup"><span data-stu-id="50957-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="50957-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50957-111">EXAMPLES</span></span>

### <span data-ttu-id="50957-112">Exempel 1: Hämta alla API-hanterings tjänster</span><span class="sxs-lookup"><span data-stu-id="50957-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="50957-113">Det här kommandot får alla API-hanterings tjänster inom ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="50957-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="50957-114">Exempel 2: Hämta alla API Management-tjänster med ett specifikt namn</span><span class="sxs-lookup"><span data-stu-id="50957-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="50957-115">Det här kommandot får alla API-hanterings tjänster efter namn.</span><span class="sxs-lookup"><span data-stu-id="50957-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="50957-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50957-116">PARAMETERS</span></span>

### <span data-ttu-id="50957-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50957-117">-DefaultProfile</span></span>
<span data-ttu-id="50957-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50957-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50957-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="50957-119">-Name</span></span>
<span data-ttu-id="50957-120">Anger namnet på API-hanteringsservern.</span><span class="sxs-lookup"><span data-stu-id="50957-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="50957-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50957-121">-ResourceGroupName</span></span>
<span data-ttu-id="50957-122">Anger namnet på den resurs grupp under vilken denna cmdlet får API Management-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="50957-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="50957-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50957-123">-ResourceId</span></span>
<span data-ttu-id="50957-124">Arm-ResourceId för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="50957-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50957-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50957-125">CommonParameters</span></span>
<span data-ttu-id="50957-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50957-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50957-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50957-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50957-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50957-128">INPUTS</span></span>

### <span data-ttu-id="50957-129">System. String</span><span class="sxs-lookup"><span data-stu-id="50957-129">System.String</span></span>

## <span data-ttu-id="50957-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50957-130">OUTPUTS</span></span>

### <span data-ttu-id="50957-131">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="50957-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="50957-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50957-132">NOTES</span></span>

## <span data-ttu-id="50957-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50957-133">RELATED LINKS</span></span>

[<span data-ttu-id="50957-134">Säkerhets kopiering-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="50957-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="50957-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="50957-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="50957-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="50957-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="50957-137">Återställ-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="50957-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


