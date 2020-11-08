---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261713"
---
# <span data-ttu-id="2923c-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="2923c-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="2923c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2923c-102">SYNOPSIS</span></span>
<span data-ttu-id="2923c-103">Hämtar regulatoey</span><span class="sxs-lookup"><span data-stu-id="2923c-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="2923c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2923c-104">SYNTAX</span></span>

### <span data-ttu-id="2923c-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="2923c-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2923c-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="2923c-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2923c-107">ID</span><span class="sxs-lookup"><span data-stu-id="2923c-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2923c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2923c-108">DESCRIPTION</span></span>
<span data-ttu-id="2923c-109">Få information om spcific myndighets efterlevnad eller lista alla regler för efterlevnad under specifika abonnemang.</span><span class="sxs-lookup"><span data-stu-id="2923c-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="2923c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2923c-110">EXAMPLES</span></span>

### <span data-ttu-id="2923c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2923c-111">Example 1</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/Azure-CIS-1.1.0
Name                : Azure-CIS-1.1.0
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 20
FailedControls      : 4
SkippedControls     : 0
UnsupportedControls : 87

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/ISO-27001
Name                : ISO-27001
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 9
FailedControls      : 10
SkippedControls     : 2
UnsupportedControls : 93

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/PCI-DSS-3.2.1
Name                : PCI-DSS-3.2.1
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 13
FailedControls      : 32
SkippedControls     : 0
UnsupportedControls : 187

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="2923c-112">Få alla regler för efterlevnad under ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="2923c-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="2923c-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2923c-113">Example 2</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -Name "SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="2923c-114">Få detaljerad information om den särskilda standarden för efterlevnad enligt standard namnet.</span><span class="sxs-lookup"><span data-stu-id="2923c-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="2923c-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="2923c-115">Example 3</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplianceStandards/SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="2923c-116">Få detaljerad information om specifika regler för regelefterlevnad enligt resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2923c-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="2923c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2923c-117">PARAMETERS</span></span>

### <span data-ttu-id="2923c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2923c-118">-DefaultProfile</span></span>
<span data-ttu-id="2923c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2923c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2923c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2923c-120">-Name</span></span>
<span data-ttu-id="2923c-121">Standard namn.</span><span class="sxs-lookup"><span data-stu-id="2923c-121">Standard name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2923c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2923c-122">-ResourceId</span></span>
<span data-ttu-id="2923c-123">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="2923c-123">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2923c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2923c-124">CommonParameters</span></span>
<span data-ttu-id="2923c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2923c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2923c-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2923c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2923c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2923c-127">INPUTS</span></span>

### <span data-ttu-id="2923c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2923c-128">System.String</span></span>

## <span data-ttu-id="2923c-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2923c-129">OUTPUTS</span></span>

### <span data-ttu-id="2923c-130">Microsoft. Azure. commands. SecurityCenter. Models. RegulatoryCompliance. PSSecurityRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="2923c-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="2923c-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2923c-131">NOTES</span></span>

## <span data-ttu-id="2923c-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2923c-132">RELATED LINKS</span></span>
