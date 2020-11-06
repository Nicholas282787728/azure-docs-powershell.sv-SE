---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 22cba1b904032ee654b091d1adae541848fd50c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573088"
---
# <span data-ttu-id="b25aa-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b25aa-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="b25aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b25aa-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b25aa-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b25aa-103">SYNTAX</span></span>

### <span data-ttu-id="b25aa-104">GetAllProperties (standard)</span><span class="sxs-lookup"><span data-stu-id="b25aa-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b25aa-105">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="b25aa-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b25aa-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="b25aa-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b25aa-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="b25aa-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b25aa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b25aa-108">DESCRIPTION</span></span>

## <span data-ttu-id="b25aa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b25aa-109">EXAMPLES</span></span>

### <span data-ttu-id="b25aa-110">Exempel 1: Hämta egenskap efter namn</span><span class="sxs-lookup"><span data-stu-id="b25aa-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="b25aa-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b25aa-111">PARAMETERS</span></span>

### <span data-ttu-id="b25aa-112">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b25aa-112">-Context</span></span>
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

### <span data-ttu-id="b25aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25aa-113">-DefaultProfile</span></span>
<span data-ttu-id="b25aa-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b25aa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b25aa-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b25aa-115">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b25aa-116">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="b25aa-116">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByPropertyId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b25aa-117">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b25aa-117">-Tag</span></span>
<span data-ttu-id="b25aa-118">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b25aa-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b25aa-119">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="b25aa-119">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b25aa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25aa-120">CommonParameters</span></span>
<span data-ttu-id="b25aa-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b25aa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25aa-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b25aa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25aa-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b25aa-123">INPUTS</span></span>

### <span data-ttu-id="b25aa-124">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b25aa-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b25aa-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b25aa-125">System.String</span></span>

## <span data-ttu-id="b25aa-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b25aa-126">OUTPUTS</span></span>

### <span data-ttu-id="b25aa-127">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b25aa-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="b25aa-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b25aa-128">NOTES</span></span>

## <span data-ttu-id="b25aa-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b25aa-129">RELATED LINKS</span></span>
