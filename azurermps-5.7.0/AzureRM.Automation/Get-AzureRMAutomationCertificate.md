---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: 012eb357b6d64964c2564dca51ac0b77a5f96880
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574453"
---
# <span data-ttu-id="76eef-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="76eef-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="76eef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76eef-102">SYNOPSIS</span></span>
<span data-ttu-id="76eef-103">Hämtar automatiserings certifikat.</span><span class="sxs-lookup"><span data-stu-id="76eef-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76eef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76eef-104">SYNTAX</span></span>

### <span data-ttu-id="76eef-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="76eef-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76eef-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="76eef-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76eef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76eef-107">DESCRIPTION</span></span>
<span data-ttu-id="76eef-108">Cmdleten **Get-AzureRmAutomationCertificate** får ett eller flera Azure Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="76eef-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="76eef-109">Denna cmdlet får som standard alla certifikat.</span><span class="sxs-lookup"><span data-stu-id="76eef-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="76eef-110">Ange namnet på ett certifikat för att få ett visst certifikat.</span><span class="sxs-lookup"><span data-stu-id="76eef-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="76eef-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76eef-111">EXAMPLES</span></span>

### <span data-ttu-id="76eef-112">Exempel 1: Hämta alla certifikat</span><span class="sxs-lookup"><span data-stu-id="76eef-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="76eef-113">Det här kommandot får metadata för alla certifikat i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="76eef-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="76eef-114">Exempel 2: skaffa ett certifikat</span><span class="sxs-lookup"><span data-stu-id="76eef-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="76eef-115">Det här kommandot får metadata för certifikatet med namnet ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="76eef-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="76eef-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76eef-116">PARAMETERS</span></span>

### <span data-ttu-id="76eef-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="76eef-117">-AutomationAccountName</span></span>
<span data-ttu-id="76eef-118">Anger namnet på det Automation-konto som denna cmdlet hämtar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="76eef-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76eef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76eef-119">-DefaultProfile</span></span>
<span data-ttu-id="76eef-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="76eef-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76eef-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="76eef-121">-Name</span></span>
<span data-ttu-id="76eef-122">Anger namnet på ett certifikat som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="76eef-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76eef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76eef-123">-ResourceGroupName</span></span>
<span data-ttu-id="76eef-124">Anger namnet på en resurs grupp för vilken denna cmdlet får ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="76eef-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76eef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76eef-125">CommonParameters</span></span>
<span data-ttu-id="76eef-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76eef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76eef-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76eef-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76eef-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76eef-128">INPUTS</span></span>

### <span data-ttu-id="76eef-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="76eef-129">None</span></span>
<span data-ttu-id="76eef-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="76eef-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76eef-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76eef-131">OUTPUTS</span></span>

### <span data-ttu-id="76eef-132">Microsoft. Azure. commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="76eef-132">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="76eef-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76eef-133">NOTES</span></span>

## <span data-ttu-id="76eef-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76eef-134">RELATED LINKS</span></span>

[<span data-ttu-id="76eef-135">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="76eef-135">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="76eef-136">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="76eef-136">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="76eef-137">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="76eef-137">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


