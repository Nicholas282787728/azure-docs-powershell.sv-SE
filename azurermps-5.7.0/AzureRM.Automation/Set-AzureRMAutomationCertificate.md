---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: a1858419b20bf85a40f94e2b5016b461cd24c39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582139"
---
# <span data-ttu-id="f0b7e-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0b7e-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="f0b7e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b7e-103">Ändrar konfigurationen för ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0b7e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0b7e-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0b7e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0b7e-105">DESCRIPTION</span></span>
<span data-ttu-id="f0b7e-106">Cmdleten **set-AzureRmAutomationCertificate** ändrar konfigurationen för ett certifikat i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="f0b7e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0b7e-107">EXAMPLES</span></span>

### <span data-ttu-id="f0b7e-108">Exempel 1: ändra ett certifikat</span><span class="sxs-lookup"><span data-stu-id="f0b7e-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f0b7e-109">Med det första kommandot konverteras ett oformaterat lösen ord till en säker sträng med hjälp av ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="f0b7e-110">Kommandot lagrar objektet i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-110">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="f0b7e-111">Det andra kommandot ändrar ett certifikat som heter ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="f0b7e-112">Kommandot använder det lösen ord som lagras i $Password.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="f0b7e-113">Kommandot anger konto namnet och sökvägen till filen som laddas upp.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="f0b7e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0b7e-114">PARAMETERS</span></span>

### <span data-ttu-id="f0b7e-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f0b7e-115">-AutomationAccountName</span></span>
<span data-ttu-id="f0b7e-116">Anger namnet på det Automation-konto som denna cmdlet ändrar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="f0b7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b7e-117">-DefaultProfile</span></span>
<span data-ttu-id="f0b7e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f0b7e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0b7e-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="f0b7e-119">-Description</span></span>
<span data-ttu-id="f0b7e-120">Anger en beskrivning för det certifikat som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b7e-121">– Kan exporteras</span><span class="sxs-lookup"><span data-stu-id="f0b7e-121">-Exportable</span></span>
<span data-ttu-id="f0b7e-122">Anger om certifikatet kan exporteras.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-122">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b7e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="f0b7e-123">-Name</span></span>
<span data-ttu-id="f0b7e-124">Anger namnet på det certifikat som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b7e-125">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="f0b7e-125">-Password</span></span>
<span data-ttu-id="f0b7e-126">Anger lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-126">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b7e-127">-Path</span><span class="sxs-lookup"><span data-stu-id="f0b7e-127">-Path</span></span>
<span data-ttu-id="f0b7e-128">Anger sökvägen till en skript fil som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="f0b7e-129">Filen kan vara en CER-fil eller en. pfx-fil.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-129">The file can be a .cer file or a .pfx file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b7e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b7e-130">-ResourceGroupName</span></span>
<span data-ttu-id="f0b7e-131">Anger namnet på den resurs grupp som den här cmdleten ändrar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="f0b7e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b7e-132">CommonParameters</span></span>
<span data-ttu-id="f0b7e-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b7e-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0b7e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b7e-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0b7e-135">INPUTS</span></span>

### <span data-ttu-id="f0b7e-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="f0b7e-136">None</span></span>
<span data-ttu-id="f0b7e-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f0b7e-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0b7e-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0b7e-138">OUTPUTS</span></span>

### <span data-ttu-id="f0b7e-139">Microsoft. Azure. commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="f0b7e-139">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="f0b7e-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0b7e-140">NOTES</span></span>

## <span data-ttu-id="f0b7e-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0b7e-141">RELATED LINKS</span></span>

[<span data-ttu-id="f0b7e-142">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0b7e-142">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="f0b7e-143">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0b7e-143">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="f0b7e-144">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0b7e-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


