---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 2624ccad63b2992ef8cae889cea04b849658444e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743416"
---
# <span data-ttu-id="473e1-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="473e1-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="473e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="473e1-102">SYNOPSIS</span></span>
<span data-ttu-id="473e1-103">Hämtar en Authorization Server för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="473e1-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="473e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="473e1-104">SYNTAX</span></span>

### <span data-ttu-id="473e1-105">GetAllAuthorizationServers (standard)</span><span class="sxs-lookup"><span data-stu-id="473e1-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="473e1-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="473e1-106">GetByServerId</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="473e1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="473e1-107">DESCRIPTION</span></span>
<span data-ttu-id="473e1-108">Cmdleten **Get-AzApiManagementAuthorizationServer** får alla auktoriseringsregler för Azure API Management eller angivna fjärrinstallationsservrar.</span><span class="sxs-lookup"><span data-stu-id="473e1-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="473e1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="473e1-109">EXAMPLES</span></span>

### <span data-ttu-id="473e1-110">Exempel 1: Hämta alla auktoriseringsregler</span><span class="sxs-lookup"><span data-stu-id="473e1-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="473e1-111">Det här kommandot får alla fjärrinstallationsservrar för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="473e1-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="473e1-112">Exempel 2: skaffa en angiven auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="473e1-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="473e1-113">Det här kommandot hämtar den angivna auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="473e1-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="473e1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="473e1-114">PARAMETERS</span></span>

### <span data-ttu-id="473e1-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="473e1-115">-Context</span></span>

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

### <span data-ttu-id="473e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="473e1-116">-DefaultProfile</span></span>
<span data-ttu-id="473e1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="473e1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="473e1-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="473e1-118">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByServerId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="473e1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473e1-119">CommonParameters</span></span>
<span data-ttu-id="473e1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="473e1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473e1-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="473e1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473e1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="473e1-122">INPUTS</span></span>

### <span data-ttu-id="473e1-123">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="473e1-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="473e1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="473e1-124">System.String</span></span>

## <span data-ttu-id="473e1-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="473e1-125">OUTPUTS</span></span>

### <span data-ttu-id="473e1-126">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="473e1-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="473e1-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="473e1-127">NOTES</span></span>

## <span data-ttu-id="473e1-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="473e1-128">RELATED LINKS</span></span>

[<span data-ttu-id="473e1-129">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="473e1-129">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="473e1-130">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="473e1-130">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="473e1-131">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="473e1-131">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


