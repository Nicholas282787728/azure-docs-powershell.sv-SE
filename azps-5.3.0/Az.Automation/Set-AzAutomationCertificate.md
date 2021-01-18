---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524873"
---
# <span data-ttu-id="d6bd4-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d6bd4-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="d6bd4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="d6bd4-103">Ändrar konfigurationen för ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="d6bd4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6bd4-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6bd4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6bd4-105">DESCRIPTION</span></span>
<span data-ttu-id="d6bd4-106">Cmdleten **set-AzAutomationCertificate** ändrar konfigurationen för ett certifikat i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="d6bd4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6bd4-107">EXAMPLES</span></span>

### <span data-ttu-id="d6bd4-108">Exempel 1: ändra ett certifikat</span><span class="sxs-lookup"><span data-stu-id="d6bd4-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d6bd4-109">Med det första kommandot konverteras ett oformaterat lösen ord till en säker sträng med hjälp av ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="d6bd4-110">Kommandot lagrar objektet i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="d6bd4-111">Det andra kommandot ändrar ett certifikat som heter ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="d6bd4-112">Kommandot använder det lösen ord som lagras i $Password.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="d6bd4-113">Kommandot anger konto namnet och sökvägen till filen som laddas upp.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="d6bd4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6bd4-114">PARAMETERS</span></span>

### <span data-ttu-id="d6bd4-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d6bd4-115">-AutomationAccountName</span></span>
<span data-ttu-id="d6bd4-116">Anger namnet på det Automation-konto som denna cmdlet ändrar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="d6bd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6bd4-117">-DefaultProfile</span></span>
<span data-ttu-id="d6bd4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d6bd4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6bd4-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d6bd4-119">-Description</span></span>
<span data-ttu-id="d6bd4-120">Anger en beskrivning för det certifikat som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bd4-121">– Kan exporteras</span><span class="sxs-lookup"><span data-stu-id="d6bd4-121">-Exportable</span></span>
<span data-ttu-id="d6bd4-122">Anger om certifikatet kan exporteras.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-122">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bd4-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6bd4-123">-Name</span></span>
<span data-ttu-id="d6bd4-124">Anger namnet på det certifikat som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bd4-125">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="d6bd4-125">-Password</span></span>
<span data-ttu-id="d6bd4-126">Anger lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-126">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bd4-127">-Path</span><span class="sxs-lookup"><span data-stu-id="d6bd4-127">-Path</span></span>
<span data-ttu-id="d6bd4-128">Anger sökvägen till en skript fil som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="d6bd4-129">Filen kan vara en CER-fil eller en. pfx-fil.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-129">The file can be a .cer file or a .pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bd4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6bd4-130">-ResourceGroupName</span></span>
<span data-ttu-id="d6bd4-131">Anger namnet på den resurs grupp som den här cmdleten ändrar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="d6bd4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6bd4-132">CommonParameters</span></span>
<span data-ttu-id="d6bd4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6bd4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6bd4-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6bd4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6bd4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6bd4-135">INPUTS</span></span>

### <span data-ttu-id="d6bd4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d6bd4-136">System.String</span></span>

### <span data-ttu-id="d6bd4-137">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d6bd4-137">System.Security.SecureString</span></span>

### <span data-ttu-id="d6bd4-138">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d6bd4-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d6bd4-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6bd4-139">OUTPUTS</span></span>

### <span data-ttu-id="d6bd4-140">Microsoft. Azure. commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="d6bd4-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="d6bd4-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6bd4-141">NOTES</span></span>

## <span data-ttu-id="d6bd4-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6bd4-142">RELATED LINKS</span></span>

[<span data-ttu-id="d6bd4-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d6bd4-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="d6bd4-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d6bd4-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="d6bd4-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d6bd4-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


