---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925938"
---
# <span data-ttu-id="ebce6-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ebce6-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="ebce6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ebce6-102">SYNOPSIS</span></span>
<span data-ttu-id="ebce6-103">Ändrar konfigurationen för ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="ebce6-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="ebce6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ebce6-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebce6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ebce6-105">DESCRIPTION</span></span>
<span data-ttu-id="ebce6-106">Cmdleten **set-AzAutomationCertificate** ändrar konfigurationen för ett certifikat i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ebce6-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="ebce6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ebce6-107">EXAMPLES</span></span>

### <span data-ttu-id="ebce6-108">Exempel 1: ändra ett certifikat</span><span class="sxs-lookup"><span data-stu-id="ebce6-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ebce6-109">Med det första kommandot konverteras ett oformaterat lösen ord till en säker sträng med hjälp av ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebce6-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="ebce6-110">Kommandot lagrar objektet i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="ebce6-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="ebce6-111">Det andra kommandot ändrar ett certifikat som heter ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="ebce6-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="ebce6-112">Kommandot använder det lösen ord som lagras i $Password.</span><span class="sxs-lookup"><span data-stu-id="ebce6-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="ebce6-113">Kommandot anger konto namnet och sökvägen till filen som laddas upp.</span><span class="sxs-lookup"><span data-stu-id="ebce6-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="ebce6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ebce6-114">PARAMETERS</span></span>

### <span data-ttu-id="ebce6-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ebce6-115">-AutomationAccountName</span></span>
<span data-ttu-id="ebce6-116">Anger namnet på det Automation-konto som denna cmdlet ändrar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="ebce6-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="ebce6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebce6-117">-DefaultProfile</span></span>
<span data-ttu-id="ebce6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ebce6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebce6-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ebce6-119">-Description</span></span>
<span data-ttu-id="ebce6-120">Anger en beskrivning för det certifikat som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="ebce6-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ebce6-121">– Kan exporteras</span><span class="sxs-lookup"><span data-stu-id="ebce6-121">-Exportable</span></span>
<span data-ttu-id="ebce6-122">Anger om certifikatet kan exporteras.</span><span class="sxs-lookup"><span data-stu-id="ebce6-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="ebce6-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="ebce6-123">-Name</span></span>
<span data-ttu-id="ebce6-124">Anger namnet på det certifikat som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="ebce6-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ebce6-125">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="ebce6-125">-Password</span></span>
<span data-ttu-id="ebce6-126">Anger lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="ebce6-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="ebce6-127">-Path</span><span class="sxs-lookup"><span data-stu-id="ebce6-127">-Path</span></span>
<span data-ttu-id="ebce6-128">Anger sökvägen till en skript fil som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="ebce6-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="ebce6-129">Filen kan vara en CER-fil eller en. pfx-fil.</span><span class="sxs-lookup"><span data-stu-id="ebce6-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="ebce6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebce6-130">-ResourceGroupName</span></span>
<span data-ttu-id="ebce6-131">Anger namnet på den resurs grupp som den här cmdleten ändrar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="ebce6-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="ebce6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebce6-132">CommonParameters</span></span>
<span data-ttu-id="ebce6-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebce6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebce6-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebce6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebce6-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ebce6-135">INPUTS</span></span>

### <span data-ttu-id="ebce6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ebce6-136">System.String</span></span>

### <span data-ttu-id="ebce6-137">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ebce6-137">System.Security.SecureString</span></span>

### <span data-ttu-id="ebce6-138">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ebce6-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ebce6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ebce6-139">OUTPUTS</span></span>

### <span data-ttu-id="ebce6-140">Microsoft. Azure. commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="ebce6-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="ebce6-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ebce6-141">NOTES</span></span>

## <span data-ttu-id="ebce6-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ebce6-142">RELATED LINKS</span></span>

[<span data-ttu-id="ebce6-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ebce6-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="ebce6-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ebce6-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="ebce6-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ebce6-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

