---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270324"
---
# <span data-ttu-id="c4db2-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="c4db2-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="c4db2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4db2-102">SYNOPSIS</span></span>
<span data-ttu-id="c4db2-103">Skapa ett nytt resurs plats avtal (används i gateways).</span><span class="sxs-lookup"><span data-stu-id="c4db2-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="c4db2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4db2-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4db2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4db2-105">DESCRIPTION</span></span>
<span data-ttu-id="c4db2-106">**New-AzApiManagementResourceLocationObject-** cmdleten skapa ett nytt resurs plats avtal (används i gateways).</span><span class="sxs-lookup"><span data-stu-id="c4db2-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="c4db2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4db2-107">EXAMPLES</span></span>

### <span data-ttu-id="c4db2-108">Exempel 1: skapa ett resurs plats kontrakt</span><span class="sxs-lookup"><span data-stu-id="c4db2-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="c4db2-109">Det här kommandot skapar en resurs plats.</span><span class="sxs-lookup"><span data-stu-id="c4db2-109">This command creates a resource location.</span></span>

## <span data-ttu-id="c4db2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4db2-110">PARAMETERS</span></span>

### <span data-ttu-id="c4db2-111">-Ort</span><span class="sxs-lookup"><span data-stu-id="c4db2-111">-City</span></span>
<span data-ttu-id="c4db2-112">Plats.</span><span class="sxs-lookup"><span data-stu-id="c4db2-112">Location City.</span></span>
<span data-ttu-id="c4db2-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c4db2-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="c4db2-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="c4db2-114">-CountryOrRegion</span></span>
<span data-ttu-id="c4db2-115">Plats land eller region.</span><span class="sxs-lookup"><span data-stu-id="c4db2-115">Location Country or Region.</span></span>
<span data-ttu-id="c4db2-116">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c4db2-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="c4db2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4db2-117">-DefaultProfile</span></span>
<span data-ttu-id="c4db2-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4db2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4db2-119">-Distriktet</span><span class="sxs-lookup"><span data-stu-id="c4db2-119">-District</span></span>
<span data-ttu-id="c4db2-120">Plats distrikt.</span><span class="sxs-lookup"><span data-stu-id="c4db2-120">Location District.</span></span>
<span data-ttu-id="c4db2-121">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c4db2-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="c4db2-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4db2-122">-Name</span></span>
<span data-ttu-id="c4db2-123">Plats namn.</span><span class="sxs-lookup"><span data-stu-id="c4db2-123">Location Name.</span></span>
<span data-ttu-id="c4db2-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c4db2-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4db2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4db2-125">CommonParameters</span></span>
<span data-ttu-id="c4db2-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4db2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4db2-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4db2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4db2-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4db2-128">INPUTS</span></span>

### <span data-ttu-id="c4db2-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="c4db2-129">None</span></span>

## <span data-ttu-id="c4db2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4db2-130">OUTPUTS</span></span>

### <span data-ttu-id="c4db2-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="c4db2-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="c4db2-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4db2-132">NOTES</span></span>

## <span data-ttu-id="c4db2-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4db2-133">RELATED LINKS</span></span>
