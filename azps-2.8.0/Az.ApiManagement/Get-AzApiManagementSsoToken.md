---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 8b8ac352819b9b3ec7cd655501c5bf8cfbba6816
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745821"
---
# <span data-ttu-id="ad851-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="ad851-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="ad851-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad851-102">SYNOPSIS</span></span>
<span data-ttu-id="ad851-103">Hämtar en länk med SSO-token till en distribuerad hanterings Portal för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ad851-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="ad851-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad851-104">SYNTAX</span></span>

### <span data-ttu-id="ad851-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="ad851-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad851-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad851-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad851-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad851-107">DESCRIPTION</span></span>
<span data-ttu-id="ad851-108">Cmdleten **Get-AzApiManagementSsoToken** returnerar en länk (URL) som innehåller en token för enkel inloggning (SSO) till en distribuerad hanterings Portal för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ad851-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="ad851-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad851-109">EXAMPLES</span></span>

### <span data-ttu-id="ad851-110">Exempel 1: Hämta SSO-token för en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="ad851-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="ad851-111">Det här kommandot får SSO-token för en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="ad851-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="ad851-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad851-112">PARAMETERS</span></span>

### <span data-ttu-id="ad851-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad851-113">-DefaultProfile</span></span>
<span data-ttu-id="ad851-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad851-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad851-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad851-115">-InputObject</span></span>
<span data-ttu-id="ad851-116">Instans av PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ad851-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="ad851-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ad851-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad851-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad851-118">-Name</span></span>
<span data-ttu-id="ad851-119">Anger namnet på API-hanterings instansen.</span><span class="sxs-lookup"><span data-stu-id="ad851-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad851-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad851-120">-ResourceGroupName</span></span>
<span data-ttu-id="ad851-121">Anger namnet på den resurs grupp som API-hantering finns under.</span><span class="sxs-lookup"><span data-stu-id="ad851-121">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad851-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad851-122">CommonParameters</span></span>
<span data-ttu-id="ad851-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad851-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad851-124">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad851-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad851-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad851-125">INPUTS</span></span>

### <span data-ttu-id="ad851-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ad851-126">System.String</span></span>

## <span data-ttu-id="ad851-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad851-127">OUTPUTS</span></span>

### <span data-ttu-id="ad851-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ad851-128">System.String</span></span>

## <span data-ttu-id="ad851-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad851-129">NOTES</span></span>

## <span data-ttu-id="ad851-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad851-130">RELATED LINKS</span></span>

[<span data-ttu-id="ad851-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad851-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


