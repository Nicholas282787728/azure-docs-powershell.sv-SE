---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 7542e9621d90ffdb19bb8db679592dd17a216d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756009"
---
# <span data-ttu-id="dfd44-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="dfd44-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="dfd44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfd44-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfd44-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfd44-103">SYNTAX</span></span>

### <span data-ttu-id="dfd44-104">Hämta alla egenskaper (standard)</span><span class="sxs-lookup"><span data-stu-id="dfd44-104">Get all properties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dfd44-105">Hämta efter egenskaps-ID</span><span class="sxs-lookup"><span data-stu-id="dfd44-105">Get by property ID</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfd44-106">Hitta egenskaper som innehåller namn</span><span class="sxs-lookup"><span data-stu-id="dfd44-106">Find properties containing Name</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfd44-107">Söka efter egenskaper efter tagg</span><span class="sxs-lookup"><span data-stu-id="dfd44-107">Find properties by Tag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfd44-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfd44-108">DESCRIPTION</span></span>

## <span data-ttu-id="dfd44-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfd44-109">EXAMPLES</span></span>

### <span data-ttu-id="dfd44-110">9.1</span><span class="sxs-lookup"><span data-stu-id="dfd44-110">1:</span></span>
```
PS C:\> Get-AzureRmApiManagementProperty -Context $Context -Name $PropertyName
```

## <span data-ttu-id="dfd44-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfd44-111">PARAMETERS</span></span>

### <span data-ttu-id="dfd44-112">-Kontext</span><span class="sxs-lookup"><span data-stu-id="dfd44-112">-Context</span></span>
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

### <span data-ttu-id="dfd44-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="dfd44-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: Find properties containing Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd44-114">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="dfd44-114">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by property ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd44-115">-Tagg</span><span class="sxs-lookup"><span data-stu-id="dfd44-115">-Tag</span></span>
<span data-ttu-id="dfd44-116">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="dfd44-116">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dfd44-117">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="dfd44-117">For example:</span></span>

<span data-ttu-id="dfd44-118">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="dfd44-118">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: Find properties by Tag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd44-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd44-119">-DefaultProfile</span></span>
<span data-ttu-id="dfd44-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dfd44-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfd44-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd44-121">CommonParameters</span></span>
<span data-ttu-id="dfd44-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfd44-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd44-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfd44-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd44-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfd44-124">INPUTS</span></span>

## <span data-ttu-id="dfd44-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfd44-125">OUTPUTS</span></span>

### <span data-ttu-id="dfd44-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="dfd44-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="dfd44-127">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="dfd44-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="dfd44-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfd44-128">NOTES</span></span>

## <span data-ttu-id="dfd44-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfd44-129">RELATED LINKS</span></span>

