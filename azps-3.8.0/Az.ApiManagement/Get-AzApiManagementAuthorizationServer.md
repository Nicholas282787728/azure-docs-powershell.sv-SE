---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 94e7889d1c59d7e132d10e8da6881dc88e612287
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089670"
---
# <span data-ttu-id="a6bf3-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a6bf3-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="a6bf3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bf3-103">Hämtar en Authorization Server för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="a6bf3-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="a6bf3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6bf3-104">SYNTAX</span></span>

### <span data-ttu-id="a6bf3-105">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a6bf3-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6bf3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6bf3-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6bf3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6bf3-107">DESCRIPTION</span></span>
<span data-ttu-id="a6bf3-108">Cmdleten **Get-AzApiManagementAuthorizationServer** får alla auktoriseringsregler för Azure API Management eller angivna fjärrinstallationsservrar.</span><span class="sxs-lookup"><span data-stu-id="a6bf3-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="a6bf3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6bf3-109">EXAMPLES</span></span>

### <span data-ttu-id="a6bf3-110">Exempel 1: Hämta alla auktoriseringsregler</span><span class="sxs-lookup"><span data-stu-id="a6bf3-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="a6bf3-111">Det här kommandot får alla fjärrinstallationsservrar för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="a6bf3-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="a6bf3-112">Exempel 2: skaffa en angiven auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="a6bf3-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="a6bf3-113">Det här kommandot hämtar den angivna auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="a6bf3-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="a6bf3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6bf3-114">PARAMETERS</span></span>

### <span data-ttu-id="a6bf3-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a6bf3-115">-Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6bf3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6bf3-116">-DefaultProfile</span></span>
<span data-ttu-id="a6bf3-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bf3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6bf3-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6bf3-118">-ResourceId</span></span>
<span data-ttu-id="a6bf3-119">Arm-resurs-ID för auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="a6bf3-119">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="a6bf3-120">Om det här alternativet anges görs ett försök att hitta auktoriseringsservern med identifieraren.</span><span class="sxs-lookup"><span data-stu-id="a6bf3-120">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="a6bf3-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a6bf3-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6bf3-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="a6bf3-122">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6bf3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6bf3-123">CommonParameters</span></span>
<span data-ttu-id="a6bf3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6bf3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6bf3-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6bf3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6bf3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6bf3-126">INPUTS</span></span>

### <span data-ttu-id="a6bf3-127">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a6bf3-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a6bf3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a6bf3-128">System.String</span></span>

## <span data-ttu-id="a6bf3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6bf3-129">OUTPUTS</span></span>

### <span data-ttu-id="a6bf3-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a6bf3-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="a6bf3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6bf3-131">NOTES</span></span>

## <span data-ttu-id="a6bf3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6bf3-132">RELATED LINKS</span></span>

[<span data-ttu-id="a6bf3-133">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a6bf3-133">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="a6bf3-134">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a6bf3-134">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="a6bf3-135">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a6bf3-135">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


