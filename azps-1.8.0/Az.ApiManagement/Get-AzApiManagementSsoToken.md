---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 40c9166ab650f7cb31ac53c55397bb7bc635f6e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743392"
---
# <span data-ttu-id="80c5f-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="80c5f-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="80c5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="80c5f-103">Hämtar en länk med SSO-token till en distribuerad hanterings Portal för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="80c5f-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="80c5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80c5f-104">SYNTAX</span></span>

```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80c5f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="80c5f-106">Cmdleten **Get-AzApiManagementSsoToken** returnerar en länk (URL) som innehåller en token för enkel inloggning (SSO) till en distribuerad hanterings Portal för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="80c5f-106">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="80c5f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80c5f-107">EXAMPLES</span></span>

### <span data-ttu-id="80c5f-108">Exempel 1: Hämta SSO-token för en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="80c5f-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="80c5f-109">Det här kommandot får SSO-token för en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="80c5f-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="80c5f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80c5f-110">PARAMETERS</span></span>

### <span data-ttu-id="80c5f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c5f-111">-DefaultProfile</span></span>
<span data-ttu-id="80c5f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80c5f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80c5f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="80c5f-113">-Name</span></span>
<span data-ttu-id="80c5f-114">Anger namnet på API-hanterings instansen.</span><span class="sxs-lookup"><span data-stu-id="80c5f-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="80c5f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c5f-115">-ResourceGroupName</span></span>
<span data-ttu-id="80c5f-116">Anger namnet på den resurs grupp som API-hantering finns under.</span><span class="sxs-lookup"><span data-stu-id="80c5f-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="80c5f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c5f-117">CommonParameters</span></span>
<span data-ttu-id="80c5f-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80c5f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c5f-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80c5f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c5f-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80c5f-120">INPUTS</span></span>

### <span data-ttu-id="80c5f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="80c5f-121">System.String</span></span>

## <span data-ttu-id="80c5f-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80c5f-122">OUTPUTS</span></span>

### <span data-ttu-id="80c5f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="80c5f-123">System.String</span></span>

## <span data-ttu-id="80c5f-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80c5f-124">NOTES</span></span>

## <span data-ttu-id="80c5f-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80c5f-125">RELATED LINKS</span></span>

[<span data-ttu-id="80c5f-126">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="80c5f-126">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


