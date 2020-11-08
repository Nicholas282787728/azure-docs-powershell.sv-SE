---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementusertoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
ms.openlocfilehash: 5b8c781380ced5ed174c094cf1ff66a8eb820309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089647"
---
# <span data-ttu-id="f78a6-101">New-AzApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="f78a6-101">New-AzApiManagementUserToken</span></span>

## <span data-ttu-id="f78a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f78a6-102">SYNOPSIS</span></span>
<span data-ttu-id="f78a6-103">Skapar en delad åtkomsttoken för användaren.</span><span class="sxs-lookup"><span data-stu-id="f78a6-103">Generates a Shared Access Token for the User.</span></span>

## <span data-ttu-id="f78a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f78a6-104">SYNTAX</span></span>

```
New-AzApiManagementUserToken -Context <PsApiManagementContext> -UserId <String>
 [-KeyType <PsApiManagementUserKeyType>] [-Expiry <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f78a6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f78a6-105">DESCRIPTION</span></span>
<span data-ttu-id="f78a6-106">Cmdlet **New-AzApiManagementUserToken** skapar en delad åtkomsttoken för en viss användare</span><span class="sxs-lookup"><span data-stu-id="f78a6-106">The cmdlet **New-AzApiManagementUserToken** generates a Shared Access Token for a specified User</span></span>

## <span data-ttu-id="f78a6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f78a6-107">EXAMPLES</span></span>

### <span data-ttu-id="f78a6-108">Exempel 1: generera en delad åtkomsttoken för git-användare</span><span class="sxs-lookup"><span data-stu-id="f78a6-108">Example 1 : Generate a Shared Access Token for Git User</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName powershelltest -ServiceName
powershellsdkservice
S D:\github\azure-powershell> $gitAccess=Get-AzApiManagementTenantAccess -Context $context
PS D:\github\azure-powershell> New-AzApiManagementUserToken -Context $context -UserId $gitAccess.Id

UserId      TokenExpiry         KeyType UserToken
------      -----------         ------- ---------
integration 5/3/2019 2:02:34 PM Primary integration&201905031402&zOwopJChWAA6oaqGHMyf7Ol9wUCPcrtdmBmff8c2lcmZk9Y...
```

<span data-ttu-id="f78a6-109">Det här manuset hämtar git-användaren som är konfigurerad i ApiManagement-tjänsten och skapar en delad åtkomsttoken med den primära nyckeln som är giltig i 8 timmar.</span><span class="sxs-lookup"><span data-stu-id="f78a6-109">This script get the Git user configured in ApiManagement service and generates a Shared Access Token using the Primary Key valid for 8 hours.</span></span>

## <span data-ttu-id="f78a6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f78a6-110">PARAMETERS</span></span>

### <span data-ttu-id="f78a6-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f78a6-111">-Context</span></span>
<span data-ttu-id="f78a6-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f78a6-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f78a6-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f78a6-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f78a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f78a6-114">-DefaultProfile</span></span>
<span data-ttu-id="f78a6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f78a6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f78a6-116">-Utgång</span><span class="sxs-lookup"><span data-stu-id="f78a6-116">-Expiry</span></span>
<span data-ttu-id="f78a6-117">Giltigheten för token.</span><span class="sxs-lookup"><span data-stu-id="f78a6-117">Expiry of the Token.</span></span>
<span data-ttu-id="f78a6-118">Om det inte anges skapas token efter 8 timmar.</span><span class="sxs-lookup"><span data-stu-id="f78a6-118">If not specified, the token is created to expire after 8 hours.</span></span>
<span data-ttu-id="f78a6-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f78a6-119">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78a6-120">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="f78a6-120">-KeyType</span></span>
<span data-ttu-id="f78a6-121">Användar nyckel att använda när du skapar token.</span><span class="sxs-lookup"><span data-stu-id="f78a6-121">User Key to use when generating the Token.</span></span>
<span data-ttu-id="f78a6-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f78a6-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78a6-123">-UserId</span><span class="sxs-lookup"><span data-stu-id="f78a6-123">-UserId</span></span>
<span data-ttu-id="f78a6-124">Identifierare för befintlig användare.</span><span class="sxs-lookup"><span data-stu-id="f78a6-124">Identifier of existing user.</span></span>
<span data-ttu-id="f78a6-125">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f78a6-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f78a6-126">CommonParameters</span></span>
<span data-ttu-id="f78a6-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f78a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f78a6-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f78a6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f78a6-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f78a6-129">INPUTS</span></span>

### <span data-ttu-id="f78a6-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f78a6-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f78a6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f78a6-131">System.String</span></span>

### <span data-ttu-id="f78a6-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserKeyType</span><span class="sxs-lookup"><span data-stu-id="f78a6-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType</span></span>

### <span data-ttu-id="f78a6-133">System. Nullable ' 1 [[system. DateTime, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f78a6-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f78a6-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f78a6-134">OUTPUTS</span></span>

### <span data-ttu-id="f78a6-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="f78a6-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserToken</span></span>

## <span data-ttu-id="f78a6-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f78a6-136">NOTES</span></span>

## <span data-ttu-id="f78a6-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f78a6-137">RELATED LINKS</span></span>
