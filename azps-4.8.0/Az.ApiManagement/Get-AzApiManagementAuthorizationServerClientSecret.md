---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: 19e49269a4ae07b39e7a2795636e51df75b54905
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261128"
---
# <span data-ttu-id="68920-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="68920-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="68920-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68920-102">SYNOPSIS</span></span>
<span data-ttu-id="68920-103">Hämtar klient hemlighet för ett API-Management-gruppserver.</span><span class="sxs-lookup"><span data-stu-id="68920-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="68920-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68920-104">SYNTAX</span></span>

### <span data-ttu-id="68920-105">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="68920-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68920-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68920-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68920-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68920-107">DESCRIPTION</span></span>
<span data-ttu-id="68920-108">Cmdleten **Get-AzApiManagementAuthorizationServerClientSecret** hämtar klient hemligheten för Azure API Management Authorization Server.</span><span class="sxs-lookup"><span data-stu-id="68920-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="68920-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68920-109">EXAMPLES</span></span>

### <span data-ttu-id="68920-110">Exempel 1: skaffa en angiven klient hemlighet per ID för en server</span><span class="sxs-lookup"><span data-stu-id="68920-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="68920-111">Det här kommandot får den angivna cient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="68920-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="68920-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68920-112">PARAMETERS</span></span>

### <span data-ttu-id="68920-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="68920-113">-Context</span></span>
<span data-ttu-id="68920-114">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="68920-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="68920-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="68920-115">This parameter is required.</span></span>

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

### <span data-ttu-id="68920-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68920-116">-DefaultProfile</span></span>
<span data-ttu-id="68920-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68920-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68920-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68920-118">-ResourceId</span></span>
<span data-ttu-id="68920-119">Arm-resurs-ID för auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="68920-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="68920-120">Om det här alternativet anges görs ett försök att hitta auktoriseringsservern med identifieraren.</span><span class="sxs-lookup"><span data-stu-id="68920-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="68920-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="68920-121">This parameter is required.</span></span>

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

### <span data-ttu-id="68920-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="68920-122">-ServerId</span></span>
<span data-ttu-id="68920-123">Identifierare för auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="68920-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="68920-124">Om det här alternativet anges visas en Authorization Server enligt ID.</span><span class="sxs-lookup"><span data-stu-id="68920-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="68920-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="68920-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="68920-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68920-126">CommonParameters</span></span>
<span data-ttu-id="68920-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68920-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68920-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68920-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68920-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68920-129">INPUTS</span></span>

### <span data-ttu-id="68920-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68920-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68920-131">System. String</span><span class="sxs-lookup"><span data-stu-id="68920-131">System.String</span></span>

## <span data-ttu-id="68920-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68920-132">OUTPUTS</span></span>

### <span data-ttu-id="68920-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="68920-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="68920-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68920-134">NOTES</span></span>

## <span data-ttu-id="68920-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68920-135">RELATED LINKS</span></span>
