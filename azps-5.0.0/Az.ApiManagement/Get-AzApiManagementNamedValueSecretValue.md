---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324071"
---
# <span data-ttu-id="12f14-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="12f14-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="12f14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12f14-102">SYNOPSIS</span></span>
<span data-ttu-id="12f14-103">Hämtar ett hemligt värde för det specifika namngivna värdet.</span><span class="sxs-lookup"><span data-stu-id="12f14-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="12f14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12f14-104">SYNTAX</span></span>

### <span data-ttu-id="12f14-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="12f14-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12f14-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="12f14-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12f14-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12f14-107">DESCRIPTION</span></span>
<span data-ttu-id="12f14-108">Hämtar ett hemligt värde för det specifika namngivna värdet.</span><span class="sxs-lookup"><span data-stu-id="12f14-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="12f14-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12f14-109">EXAMPLES</span></span>

### <span data-ttu-id="12f14-110">Exempel 1: Hämta namngivet värde efter namn</span><span class="sxs-lookup"><span data-stu-id="12f14-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="12f14-111">Med det här kommandot hämtas den namngivna värde informationen till det namngivna värde namnet.</span><span class="sxs-lookup"><span data-stu-id="12f14-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="12f14-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12f14-112">PARAMETERS</span></span>

### <span data-ttu-id="12f14-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="12f14-113">-Context</span></span>
<span data-ttu-id="12f14-114">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="12f14-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="12f14-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="12f14-115">This parameter is required.</span></span>

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

### <span data-ttu-id="12f14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f14-116">-DefaultProfile</span></span>
<span data-ttu-id="12f14-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12f14-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f14-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="12f14-118">-NamedValueId</span></span>
<span data-ttu-id="12f14-119">Identifierare för det namngivna värdet.</span><span class="sxs-lookup"><span data-stu-id="12f14-119">Identifier of a the named value.</span></span>
<span data-ttu-id="12f14-120">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="12f14-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12f14-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f14-121">CommonParameters</span></span>
<span data-ttu-id="12f14-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f14-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f14-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12f14-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f14-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12f14-124">INPUTS</span></span>

### <span data-ttu-id="12f14-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="12f14-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="12f14-126">System. String</span><span class="sxs-lookup"><span data-stu-id="12f14-126">System.String</span></span>

## <span data-ttu-id="12f14-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12f14-127">OUTPUTS</span></span>

### <span data-ttu-id="12f14-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="12f14-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="12f14-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12f14-129">NOTES</span></span>

## <span data-ttu-id="12f14-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12f14-130">RELATED LINKS</span></span>
