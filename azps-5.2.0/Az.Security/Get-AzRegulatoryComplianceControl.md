---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
ms.openlocfilehash: 11c6c1073f53ba4a4b93fdae02ae6f6eb22e0f04
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391467"
---
# <span data-ttu-id="80eb4-101">Get-AzRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="80eb4-101">Get-AzRegulatoryComplianceControl</span></span>

## <span data-ttu-id="80eb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="80eb4-103">Hämtar regler för kontroll av efterlevnad</span><span class="sxs-lookup"><span data-stu-id="80eb4-103">Gets regulatory compliance controls</span></span>

## <span data-ttu-id="80eb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80eb4-104">SYNTAX</span></span>

### <span data-ttu-id="80eb4-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="80eb4-105">SubscriptionLevelResource (Default)</span></span>
```
Get-AzRegulatoryComplianceControl [-Name <String>] -StandardName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80eb4-106">ID</span><span class="sxs-lookup"><span data-stu-id="80eb4-106">ResourceId</span></span>
```
Get-AzRegulatoryComplianceControl -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80eb4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80eb4-107">DESCRIPTION</span></span>
<span data-ttu-id="80eb4-108">Få en spcific kontroll information eller lista alla kontroller under särskilda regler för efterlevnad.</span><span class="sxs-lookup"><span data-stu-id="80eb4-108">Get a spcific control details or list all the controls under specific regulatory compliance standard.</span></span>

## <span data-ttu-id="80eb4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80eb4-109">EXAMPLES</span></span>

### <span data-ttu-id="80eb4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="80eb4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.1
Name               : A1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Current processing capacity and usage are maintained, monitored, and evaluated to manage capacity
                     demand and to enable the implementation of additional capacity to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.2
Name               : A1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Environmental protections, software, data backup processes, and recovery infrastructure are
                     designed, developed, implemented, operated, maintained, and monitored to meet availability
                     commitments and requirements.
State              : Passed
PassedAssessments  : 3
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.3
Name               : A1.3
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Recovery plan procedures supporting system recovery are tested to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.1
Name               : C1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information is protected during the system design, development, testing,
                     implementation, and change processes in accordance with confidentiality commitments and
                     requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0
```

<span data-ttu-id="80eb4-111">Få alla kontroller under specifik regel standard.</span><span class="sxs-lookup"><span data-stu-id="80eb4-111">Get all controls under specific regulatory standard.</span></span>

### <span data-ttu-id="80eb4-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="80eb4-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP" -Name "C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="80eb4-113">Få specifik kontroll information enligt kontroll-ID.</span><span class="sxs-lookup"><span data-stu-id="80eb4-113">Get specific control details according to control id.</span></span>

### <span data-ttu-id="80eb4-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="80eb4-114">Example 3</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="80eb4-115">Få specifik kontroll information baserat på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="80eb4-115">Get specific control details according to resource id.</span></span>

## <span data-ttu-id="80eb4-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80eb4-116">PARAMETERS</span></span>

### <span data-ttu-id="80eb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80eb4-117">-DefaultProfile</span></span>
<span data-ttu-id="80eb4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80eb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80eb4-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="80eb4-119">-Name</span></span>
<span data-ttu-id="80eb4-120">Kontroll-ID.</span><span class="sxs-lookup"><span data-stu-id="80eb4-120">Control Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80eb4-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80eb4-121">-ResourceId</span></span>
<span data-ttu-id="80eb4-122">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="80eb4-122">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="80eb4-123">-StandardName</span><span class="sxs-lookup"><span data-stu-id="80eb4-123">-StandardName</span></span>
<span data-ttu-id="80eb4-124">Standard namn.</span><span class="sxs-lookup"><span data-stu-id="80eb4-124">Standard Name.</span></span>

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

### <span data-ttu-id="80eb4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80eb4-125">CommonParameters</span></span>
<span data-ttu-id="80eb4-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80eb4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80eb4-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80eb4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80eb4-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80eb4-128">INPUTS</span></span>

### <span data-ttu-id="80eb4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="80eb4-129">System.String</span></span>

## <span data-ttu-id="80eb4-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80eb4-130">OUTPUTS</span></span>

### <span data-ttu-id="80eb4-131">Microsoft. Azure. commands. SecurityCenter. Models. RegulatoryCompliance. PSSecurityRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="80eb4-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span></span>

## <span data-ttu-id="80eb4-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80eb4-132">NOTES</span></span>

## <span data-ttu-id="80eb4-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80eb4-133">RELATED LINKS</span></span>
