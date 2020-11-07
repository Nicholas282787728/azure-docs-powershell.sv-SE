---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: 956569d407918d0891af6aa1d6f8f09eb61b9a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757507"
---
# <span data-ttu-id="d9d01-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d9d01-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="d9d01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9d01-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d01-103">Hämtar automatiserings certifikat.</span><span class="sxs-lookup"><span data-stu-id="d9d01-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9d01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9d01-104">SYNTAX</span></span>

### <span data-ttu-id="d9d01-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="d9d01-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9d01-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="d9d01-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9d01-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9d01-107">DESCRIPTION</span></span>
<span data-ttu-id="d9d01-108">Cmdleten **Get-AzureRmAutomationCertificate** får ett eller flera Azure Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="d9d01-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="d9d01-109">Denna cmdlet får som standard alla certifikat.</span><span class="sxs-lookup"><span data-stu-id="d9d01-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="d9d01-110">Ange namnet på ett certifikat för att få ett visst certifikat.</span><span class="sxs-lookup"><span data-stu-id="d9d01-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="d9d01-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9d01-111">EXAMPLES</span></span>

### <span data-ttu-id="d9d01-112">Exempel 1: Hämta alla certifikat</span><span class="sxs-lookup"><span data-stu-id="d9d01-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d9d01-113">Det här kommandot får metadata för alla certifikat i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d9d01-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d9d01-114">Exempel 2: skaffa ett certifikat</span><span class="sxs-lookup"><span data-stu-id="d9d01-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="d9d01-115">Det här kommandot får metadata för certifikatet med namnet ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="d9d01-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="d9d01-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9d01-116">PARAMETERS</span></span>

### <span data-ttu-id="d9d01-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d9d01-117">-AutomationAccountName</span></span>
<span data-ttu-id="d9d01-118">Anger namnet på det Automation-konto som denna cmdlet hämtar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="d9d01-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="d9d01-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9d01-119">-Name</span></span>
<span data-ttu-id="d9d01-120">Anger namnet på ett certifikat som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="d9d01-120">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="d9d01-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9d01-121">-ResourceGroupName</span></span>
<span data-ttu-id="d9d01-122">Anger namnet på en resurs grupp för vilken denna cmdlet får ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="d9d01-122">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="d9d01-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d01-123">-DefaultProfile</span></span>
<span data-ttu-id="d9d01-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d01-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d01-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d01-125">CommonParameters</span></span>
<span data-ttu-id="d9d01-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9d01-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d01-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9d01-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d01-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9d01-128">INPUTS</span></span>

## <span data-ttu-id="d9d01-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9d01-129">OUTPUTS</span></span>

### <span data-ttu-id="d9d01-130">Microsoft. Azure. commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="d9d01-130">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="d9d01-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9d01-131">NOTES</span></span>

## <span data-ttu-id="d9d01-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9d01-132">RELATED LINKS</span></span>

[<span data-ttu-id="d9d01-133">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d9d01-133">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="d9d01-134">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d9d01-134">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="d9d01-135">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d9d01-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


