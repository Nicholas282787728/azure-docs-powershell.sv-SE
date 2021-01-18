---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525077"
---
# <span data-ttu-id="5a993-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="5a993-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="5a993-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a993-102">SYNOPSIS</span></span>
<span data-ttu-id="5a993-103">Hämtar en länk med SSO-token till en distribuerad hanterings Portal för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5a993-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="5a993-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a993-104">SYNTAX</span></span>

### <span data-ttu-id="5a993-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="5a993-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a993-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5a993-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a993-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a993-107">DESCRIPTION</span></span>
<span data-ttu-id="5a993-108">Cmdleten **Get-AzApiManagementSsoToken** returnerar en länk (URL) som innehåller en token för enkel inloggning (SSO) till en distribuerad hanterings Portal för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5a993-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="5a993-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a993-109">EXAMPLES</span></span>

### <span data-ttu-id="5a993-110">Exempel 1: Hämta SSO-token för en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="5a993-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="5a993-111">Det här kommandot får SSO-token för en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="5a993-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="5a993-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a993-112">PARAMETERS</span></span>

### <span data-ttu-id="5a993-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a993-113">-DefaultProfile</span></span>
<span data-ttu-id="5a993-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a993-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a993-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a993-115">-InputObject</span></span>
<span data-ttu-id="5a993-116">Instans av PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="5a993-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="5a993-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="5a993-117">This parameter is required.</span></span>

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

### <span data-ttu-id="5a993-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a993-118">-Name</span></span>
<span data-ttu-id="5a993-119">Anger namnet på API-hanterings instansen.</span><span class="sxs-lookup"><span data-stu-id="5a993-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="5a993-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a993-120">-ResourceGroupName</span></span>
<span data-ttu-id="5a993-121">Anger namnet på den resurs grupp som API-hantering finns under.</span><span class="sxs-lookup"><span data-stu-id="5a993-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="5a993-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a993-122">CommonParameters</span></span>
<span data-ttu-id="5a993-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a993-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a993-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a993-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a993-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a993-125">INPUTS</span></span>

### <span data-ttu-id="5a993-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5a993-126">System.String</span></span>

## <span data-ttu-id="5a993-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a993-127">OUTPUTS</span></span>

### <span data-ttu-id="5a993-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5a993-128">System.String</span></span>

## <span data-ttu-id="5a993-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a993-129">NOTES</span></span>

## <span data-ttu-id="5a993-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a993-130">RELATED LINKS</span></span>

[<span data-ttu-id="5a993-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a993-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


