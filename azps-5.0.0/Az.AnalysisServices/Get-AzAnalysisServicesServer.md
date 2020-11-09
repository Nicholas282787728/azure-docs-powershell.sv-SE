---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324131"
---
# <span data-ttu-id="62c00-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="62c00-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="62c00-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62c00-102">SYNOPSIS</span></span>
<span data-ttu-id="62c00-103">Hämtar information om en Analysis Services-server.</span><span class="sxs-lookup"><span data-stu-id="62c00-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="62c00-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62c00-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62c00-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62c00-105">DESCRIPTION</span></span>
<span data-ttu-id="62c00-106">Get-AzAnalysisServicesServer cmdlet får information om en Analysis Services-server.</span><span class="sxs-lookup"><span data-stu-id="62c00-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="62c00-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62c00-107">EXAMPLES</span></span>

### <span data-ttu-id="62c00-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="62c00-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="62c00-109">Det här kommandot får alla Azure Analysis Services-servrar i resurs gruppen "ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="62c00-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="62c00-110">Exempel 2: skaffa en server</span><span class="sxs-lookup"><span data-stu-id="62c00-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="62c00-111">Det här kommandot får Azure Analysis Services-servern med namnet testserver i resurs gruppen med namnet ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="62c00-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="62c00-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62c00-112">PARAMETERS</span></span>

### <span data-ttu-id="62c00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c00-113">-DefaultProfile</span></span>
<span data-ttu-id="62c00-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62c00-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62c00-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="62c00-115">-Name</span></span>
<span data-ttu-id="62c00-116">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="62c00-116">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c00-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c00-117">-ResourceGroupName</span></span>
<span data-ttu-id="62c00-118">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="62c00-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c00-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c00-119">CommonParameters</span></span>
<span data-ttu-id="62c00-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62c00-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c00-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c00-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c00-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62c00-122">INPUTS</span></span>

### <span data-ttu-id="62c00-123">System. String</span><span class="sxs-lookup"><span data-stu-id="62c00-123">System.String</span></span>

## <span data-ttu-id="62c00-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62c00-124">OUTPUTS</span></span>

### <span data-ttu-id="62c00-125">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="62c00-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="62c00-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62c00-126">NOTES</span></span>
<span data-ttu-id="62c00-127">Alias: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="62c00-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="62c00-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62c00-128">RELATED LINKS</span></span>

[<span data-ttu-id="62c00-129">New-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="62c00-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="62c00-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="62c00-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
