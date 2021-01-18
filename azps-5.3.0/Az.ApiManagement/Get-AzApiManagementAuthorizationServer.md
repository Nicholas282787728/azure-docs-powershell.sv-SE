---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525120"
---
# <span data-ttu-id="47473-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="47473-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="47473-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47473-102">SYNOPSIS</span></span>
<span data-ttu-id="47473-103">Hämtar en Authorization Server för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="47473-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="47473-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47473-104">SYNTAX</span></span>

### <span data-ttu-id="47473-105">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="47473-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47473-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47473-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47473-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47473-107">DESCRIPTION</span></span>
<span data-ttu-id="47473-108">Cmdleten **Get-AzApiManagementAuthorizationServer** får alla auktoriseringsregler för Azure API Management eller den angivna auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="47473-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="47473-109">ClientSecret tas inte med i resultatet.</span><span class="sxs-lookup"><span data-stu-id="47473-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="47473-110">Använd **Get-AzApiManagementAuthorizationServerClientSecret** för att få klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="47473-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="47473-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47473-111">EXAMPLES</span></span>

### <span data-ttu-id="47473-112">Exempel 1: Hämta alla auktoriseringsregler</span><span class="sxs-lookup"><span data-stu-id="47473-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="47473-113">Det här kommandot får alla fjärrinstallationsservrar för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="47473-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="47473-114">Exempel 2: skaffa en angiven auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="47473-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="47473-115">Det här kommandot hämtar den angivna auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="47473-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="47473-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47473-116">PARAMETERS</span></span>

### <span data-ttu-id="47473-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="47473-117">-Context</span></span>

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

### <span data-ttu-id="47473-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47473-118">-DefaultProfile</span></span>
<span data-ttu-id="47473-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47473-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47473-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47473-120">-ResourceId</span></span>
<span data-ttu-id="47473-121">Arm-resurs-ID för auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="47473-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="47473-122">Om det här alternativet anges görs ett försök att hitta auktoriseringsservern med identifieraren.</span><span class="sxs-lookup"><span data-stu-id="47473-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="47473-123">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="47473-123">This parameter is required.</span></span>

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

### <span data-ttu-id="47473-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="47473-124">-ServerId</span></span>
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

### <span data-ttu-id="47473-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47473-125">CommonParameters</span></span>
<span data-ttu-id="47473-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47473-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47473-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47473-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47473-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47473-128">INPUTS</span></span>

### <span data-ttu-id="47473-129">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47473-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47473-130">System. String</span><span class="sxs-lookup"><span data-stu-id="47473-130">System.String</span></span>

## <span data-ttu-id="47473-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47473-131">OUTPUTS</span></span>

### <span data-ttu-id="47473-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="47473-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="47473-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47473-133">NOTES</span></span>

## <span data-ttu-id="47473-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47473-134">RELATED LINKS</span></span>

[<span data-ttu-id="47473-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="47473-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="47473-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="47473-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="47473-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="47473-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


