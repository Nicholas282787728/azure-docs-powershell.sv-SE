---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093389"
---
# <span data-ttu-id="ba79a-101">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba79a-101">Get-AzureAutomationCertificate</span></span>

## <span data-ttu-id="ba79a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba79a-102">SYNOPSIS</span></span>

<span data-ttu-id="ba79a-103">Får ett Azure Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="ba79a-103">Gets an Azure Automation certificate.</span></span>

## <span data-ttu-id="ba79a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba79a-104">SYNTAX</span></span>

### <span data-ttu-id="ba79a-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="ba79a-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ba79a-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="ba79a-106">ByCertificateName</span></span>
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba79a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba79a-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ba79a-108">Cmdleten **Get-AzureAutomationCertificate** får ett eller flera Microsoft Azure Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="ba79a-108">The **Get-AzureAutomationCertificate** cmdlet gets one or more Microsoft Azure Automation certificates.</span></span>
<span data-ttu-id="ba79a-109">Som standard returneras alla certifikat.</span><span class="sxs-lookup"><span data-stu-id="ba79a-109">By default, all certificates are returned.</span></span>
<span data-ttu-id="ba79a-110">Om du vill skaffa ett visst certifikat anger du dess namn.</span><span class="sxs-lookup"><span data-stu-id="ba79a-110">To get a specific certificate, specify its name.</span></span>

## <span data-ttu-id="ba79a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba79a-111">EXAMPLES</span></span>

### <span data-ttu-id="ba79a-112">Exempel 1: Hämta alla certifikat</span><span class="sxs-lookup"><span data-stu-id="ba79a-112">Example 1: Get all certificates</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

<span data-ttu-id="ba79a-113">Det här kommandot får alla certifikat i Azure Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ba79a-113">This command gets all certificates in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="ba79a-114">Exempel 2: skaffa ett certifikat</span><span class="sxs-lookup"><span data-stu-id="ba79a-114">Example 2: Get a certificate</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

<span data-ttu-id="ba79a-115">Det här kommandot får certifikatet som heter MyUserCertificate.</span><span class="sxs-lookup"><span data-stu-id="ba79a-115">This command gets the certificate named MyUserCertificate.</span></span>

## <span data-ttu-id="ba79a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba79a-116">PARAMETERS</span></span>

### <span data-ttu-id="ba79a-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ba79a-117">-AutomationAccountName</span></span>
<span data-ttu-id="ba79a-118">Anger namnet på Automation-kontot med certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ba79a-118">Specifies the name of the automation account with the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba79a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ba79a-119">-Name</span></span>
<span data-ttu-id="ba79a-120">Anger namnet på ett certifikat som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="ba79a-120">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba79a-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="ba79a-121">-Profile</span></span>
<span data-ttu-id="ba79a-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ba79a-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba79a-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ba79a-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba79a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba79a-124">CommonParameters</span></span>
<span data-ttu-id="ba79a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba79a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba79a-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba79a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba79a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba79a-127">INPUTS</span></span>

## <span data-ttu-id="ba79a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba79a-128">OUTPUTS</span></span>

### <span data-ttu-id="ba79a-129">Microsoft. Azure. commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="ba79a-129">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="ba79a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba79a-130">NOTES</span></span>

## <span data-ttu-id="ba79a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba79a-131">RELATED LINKS</span></span>

[<span data-ttu-id="ba79a-132">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba79a-132">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="ba79a-133">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba79a-133">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="ba79a-134">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba79a-134">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


