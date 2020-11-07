---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: ad6e2aebcc5a4edcf5acd3255385b0e78f317627
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743396"
---
# <span data-ttu-id="4ca4e-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4ca4e-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="4ca4e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ca4e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca4e-103">Hämtar en lista eller en viss egenskap (namngivet-värde).</span><span class="sxs-lookup"><span data-stu-id="4ca4e-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="4ca4e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ca4e-104">SYNTAX</span></span>

### <span data-ttu-id="4ca4e-105">GetAllProperties (standard)</span><span class="sxs-lookup"><span data-stu-id="4ca4e-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ca4e-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="4ca4e-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ca4e-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="4ca4e-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ca4e-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="4ca4e-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ca4e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ca4e-109">DESCRIPTION</span></span>
<span data-ttu-id="4ca4e-110">Cmdleten **Get-AzApiManagementProperty** hämtar en lista eller en speciell egenskap.</span><span class="sxs-lookup"><span data-stu-id="4ca4e-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="4ca4e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ca4e-111">EXAMPLES</span></span>

### <span data-ttu-id="4ca4e-112">Exempel 1: Hämta egenskap efter namn</span><span class="sxs-lookup"><span data-stu-id="4ca4e-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="4ca4e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ca4e-113">PARAMETERS</span></span>

### <span data-ttu-id="4ca4e-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4ca4e-114">-Context</span></span>
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

### <span data-ttu-id="4ca4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca4e-115">-DefaultProfile</span></span>
<span data-ttu-id="4ca4e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca4e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ca4e-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ca4e-117">-Name</span></span>
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

### <span data-ttu-id="4ca4e-118">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="4ca4e-118">-PropertyId</span></span>
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

### <span data-ttu-id="4ca4e-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4ca4e-119">-Tag</span></span>
<span data-ttu-id="4ca4e-120">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4ca4e-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4ca4e-121">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="4ca4e-121">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4ca4e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca4e-122">CommonParameters</span></span>
<span data-ttu-id="4ca4e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca4e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca4e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca4e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca4e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ca4e-125">INPUTS</span></span>

### <span data-ttu-id="4ca4e-126">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4ca4e-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4ca4e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4ca4e-127">System.String</span></span>

## <span data-ttu-id="4ca4e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ca4e-128">OUTPUTS</span></span>

### <span data-ttu-id="4ca4e-129">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4ca4e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="4ca4e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ca4e-130">NOTES</span></span>

## <span data-ttu-id="4ca4e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ca4e-131">RELATED LINKS</span></span>
