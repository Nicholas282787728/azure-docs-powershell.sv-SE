---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ce401334b03620ac565c5dd3b737b7a2982575e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745848"
---
# <span data-ttu-id="e0637-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e0637-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="e0637-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0637-102">SYNOPSIS</span></span>
<span data-ttu-id="e0637-103">Hämtar en Authorization Server för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="e0637-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="e0637-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0637-104">SYNTAX</span></span>

### <span data-ttu-id="e0637-105">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e0637-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0637-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0637-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0637-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0637-107">DESCRIPTION</span></span>
<span data-ttu-id="e0637-108">Cmdleten **Get-AzApiManagementAuthorizationServer** får alla auktoriseringsregler för Azure API Management eller angivna fjärrinstallationsservrar.</span><span class="sxs-lookup"><span data-stu-id="e0637-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="e0637-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0637-109">EXAMPLES</span></span>

### <span data-ttu-id="e0637-110">Exempel 1: Hämta alla auktoriseringsregler</span><span class="sxs-lookup"><span data-stu-id="e0637-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="e0637-111">Det här kommandot får alla fjärrinstallationsservrar för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="e0637-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="e0637-112">Exempel 2: skaffa en angiven auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="e0637-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="e0637-113">Det här kommandot hämtar den angivna auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="e0637-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="e0637-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0637-114">PARAMETERS</span></span>

### <span data-ttu-id="e0637-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e0637-115">-Context</span></span>

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

### <span data-ttu-id="e0637-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0637-116">-DefaultProfile</span></span>
<span data-ttu-id="e0637-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0637-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0637-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0637-118">-ResourceId</span></span>
<span data-ttu-id="e0637-119">Arm-resurs-ID för auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="e0637-119">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="e0637-120">Om det här alternativet anges görs ett försök att hitta auktoriseringsservern med identifieraren.</span><span class="sxs-lookup"><span data-stu-id="e0637-120">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="e0637-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e0637-121">This parameter is required.</span></span>

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

### <span data-ttu-id="e0637-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="e0637-122">-ServerId</span></span>
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

### <span data-ttu-id="e0637-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0637-123">CommonParameters</span></span>
<span data-ttu-id="e0637-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0637-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0637-125">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0637-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0637-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0637-126">INPUTS</span></span>

### <span data-ttu-id="e0637-127">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e0637-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e0637-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e0637-128">System.String</span></span>

## <span data-ttu-id="e0637-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0637-129">OUTPUTS</span></span>

### <span data-ttu-id="e0637-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e0637-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="e0637-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0637-131">NOTES</span></span>

## <span data-ttu-id="e0637-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0637-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0637-133">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e0637-133">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="e0637-134">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e0637-134">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="e0637-135">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e0637-135">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


