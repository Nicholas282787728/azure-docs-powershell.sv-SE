---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090448"
---
# <span data-ttu-id="0ab40-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0ab40-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="0ab40-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ab40-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab40-103">Hämtar automatiserings certifikat.</span><span class="sxs-lookup"><span data-stu-id="0ab40-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="0ab40-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ab40-104">SYNTAX</span></span>

### <span data-ttu-id="0ab40-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="0ab40-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ab40-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="0ab40-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ab40-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ab40-107">DESCRIPTION</span></span>
<span data-ttu-id="0ab40-108">Cmdleten **Get-AzAutomationCertificate** får ett eller flera Azure Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="0ab40-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="0ab40-109">Denna cmdlet får som standard alla certifikat.</span><span class="sxs-lookup"><span data-stu-id="0ab40-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="0ab40-110">Ange namnet på ett certifikat för att få ett visst certifikat.</span><span class="sxs-lookup"><span data-stu-id="0ab40-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="0ab40-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ab40-111">EXAMPLES</span></span>

### <span data-ttu-id="0ab40-112">Exempel 1: Hämta alla certifikat</span><span class="sxs-lookup"><span data-stu-id="0ab40-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="0ab40-113">Det här kommandot får metadata för alla certifikat i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0ab40-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0ab40-114">Exempel 2: skaffa ett certifikat</span><span class="sxs-lookup"><span data-stu-id="0ab40-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="0ab40-115">Det här kommandot får metadata för certifikatet med namnet ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="0ab40-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="0ab40-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ab40-116">PARAMETERS</span></span>

### <span data-ttu-id="0ab40-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0ab40-117">-AutomationAccountName</span></span>
<span data-ttu-id="0ab40-118">Anger namnet på det Automation-konto som denna cmdlet hämtar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="0ab40-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ab40-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab40-119">-DefaultProfile</span></span>
<span data-ttu-id="0ab40-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0ab40-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ab40-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ab40-121">-Name</span></span>
<span data-ttu-id="0ab40-122">Anger namnet på ett certifikat som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="0ab40-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ab40-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ab40-123">-ResourceGroupName</span></span>
<span data-ttu-id="0ab40-124">Anger namnet på en resurs grupp för vilken denna cmdlet får ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="0ab40-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ab40-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab40-125">CommonParameters</span></span>
<span data-ttu-id="0ab40-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab40-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab40-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab40-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab40-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ab40-128">INPUTS</span></span>

### <span data-ttu-id="0ab40-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0ab40-129">System.String</span></span>

## <span data-ttu-id="0ab40-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ab40-130">OUTPUTS</span></span>

### <span data-ttu-id="0ab40-131">Microsoft. Azure. commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="0ab40-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="0ab40-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ab40-132">NOTES</span></span>

## <span data-ttu-id="0ab40-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ab40-133">RELATED LINKS</span></span>

[<span data-ttu-id="0ab40-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0ab40-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="0ab40-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0ab40-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="0ab40-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0ab40-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


