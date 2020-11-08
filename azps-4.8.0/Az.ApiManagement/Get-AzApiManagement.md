---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261942"
---
# <span data-ttu-id="b3623-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3623-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="b3623-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3623-102">SYNOPSIS</span></span>
<span data-ttu-id="b3623-103">Hämtar en lista eller en särskild beskrivning för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b3623-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="b3623-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3623-104">SYNTAX</span></span>

### <span data-ttu-id="b3623-105">GetBySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="b3623-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3623-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b3623-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3623-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="b3623-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3623-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3623-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3623-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3623-109">DESCRIPTION</span></span>
<span data-ttu-id="b3623-110">Cmdleten **Get-AzApiManagement** hämtar en lista över alla API-hanterings tjänster under prenumeration eller angiven resurs grupp eller en särskild API-hantering.</span><span class="sxs-lookup"><span data-stu-id="b3623-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="b3623-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3623-111">EXAMPLES</span></span>

### <span data-ttu-id="b3623-112">Exempel 1: Hämta alla API-hanterings tjänster</span><span class="sxs-lookup"><span data-stu-id="b3623-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="b3623-113">Det här kommandot får alla API-hanterings tjänster inom ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="b3623-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="b3623-114">Exempel 2: Hämta alla API Management-tjänster med ett specifikt namn</span><span class="sxs-lookup"><span data-stu-id="b3623-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="b3623-115">Det här kommandot får alla API-hanterings tjänster efter namn.</span><span class="sxs-lookup"><span data-stu-id="b3623-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="b3623-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3623-116">PARAMETERS</span></span>

### <span data-ttu-id="b3623-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3623-117">-DefaultProfile</span></span>
<span data-ttu-id="b3623-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3623-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3623-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3623-119">-Name</span></span>
<span data-ttu-id="b3623-120">Anger namnet på API-hanteringsservern.</span><span class="sxs-lookup"><span data-stu-id="b3623-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="b3623-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3623-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3623-122">Anger namnet på den resurs grupp under vilken denna cmdlet får API Management-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b3623-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="b3623-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3623-123">-ResourceId</span></span>
<span data-ttu-id="b3623-124">Arm-ResourceId för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b3623-124">Arm ResourceId of the API Management service.</span></span>

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

### <span data-ttu-id="b3623-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3623-125">CommonParameters</span></span>
<span data-ttu-id="b3623-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3623-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3623-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3623-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3623-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3623-128">INPUTS</span></span>

### <span data-ttu-id="b3623-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b3623-129">System.String</span></span>

## <span data-ttu-id="b3623-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3623-130">OUTPUTS</span></span>

### <span data-ttu-id="b3623-131">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3623-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b3623-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3623-132">NOTES</span></span>

## <span data-ttu-id="b3623-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3623-133">RELATED LINKS</span></span>

[<span data-ttu-id="b3623-134">Säkerhets kopiering-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3623-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="b3623-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3623-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="b3623-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3623-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="b3623-137">Återställ-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3623-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


