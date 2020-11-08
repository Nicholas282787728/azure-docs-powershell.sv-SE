---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: a1ca7766efc79d3d9db2d8feef94a2bb7aab9c36
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089648"
---
# <span data-ttu-id="31540-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="31540-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="31540-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31540-102">SYNOPSIS</span></span>
<span data-ttu-id="31540-103">Hämtar en lista eller en viss egenskap (namngivet-värde).</span><span class="sxs-lookup"><span data-stu-id="31540-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="31540-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31540-104">SYNTAX</span></span>

### <span data-ttu-id="31540-105">GetAllProperties (standard)</span><span class="sxs-lookup"><span data-stu-id="31540-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31540-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="31540-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31540-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="31540-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31540-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="31540-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31540-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31540-109">DESCRIPTION</span></span>
<span data-ttu-id="31540-110">Cmdleten **Get-AzApiManagementProperty** hämtar en lista eller en speciell egenskap.</span><span class="sxs-lookup"><span data-stu-id="31540-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="31540-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31540-111">EXAMPLES</span></span>

### <span data-ttu-id="31540-112">Exempel 1: Hämta egenskap efter namn</span><span class="sxs-lookup"><span data-stu-id="31540-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="31540-113">Det här kommandot får egenskaps informationen angiven som egenskaps namn.</span><span class="sxs-lookup"><span data-stu-id="31540-113">This command gets the property details given the property name.</span></span>

## <span data-ttu-id="31540-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31540-114">PARAMETERS</span></span>

### <span data-ttu-id="31540-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="31540-115">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31540-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31540-116">-DefaultProfile</span></span>
<span data-ttu-id="31540-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31540-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31540-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="31540-118">-Name</span></span>
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

### <span data-ttu-id="31540-119">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="31540-119">-PropertyId</span></span>
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

### <span data-ttu-id="31540-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="31540-120">-Tag</span></span>
<span data-ttu-id="31540-121">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="31540-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="31540-122">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="31540-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="31540-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31540-123">CommonParameters</span></span>
<span data-ttu-id="31540-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31540-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31540-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31540-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31540-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31540-126">INPUTS</span></span>

### <span data-ttu-id="31540-127">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="31540-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="31540-128">System. String</span><span class="sxs-lookup"><span data-stu-id="31540-128">System.String</span></span>

## <span data-ttu-id="31540-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31540-129">OUTPUTS</span></span>

### <span data-ttu-id="31540-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="31540-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="31540-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31540-131">NOTES</span></span>

## <span data-ttu-id="31540-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31540-132">RELATED LINKS</span></span>
