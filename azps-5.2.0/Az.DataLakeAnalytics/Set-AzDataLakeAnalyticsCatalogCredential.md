---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 8d188e2f19c04792ea29cadef9d9ef71c20cfce9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401376"
---
# <span data-ttu-id="e3524-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="e3524-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="e3524-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3524-102">SYNOPSIS</span></span>
<span data-ttu-id="e3524-103">Ändrar lösen ordet för Azure Data Lake Analytics-katalogen.</span><span class="sxs-lookup"><span data-stu-id="e3524-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="e3524-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3524-104">SYNTAX</span></span>

### <span data-ttu-id="e3524-105">SetByHostNameAndPort (standard)</span><span class="sxs-lookup"><span data-stu-id="e3524-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3524-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="e3524-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3524-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3524-107">DESCRIPTION</span></span>
<span data-ttu-id="e3524-108">Set-AzDataLakeAnalyticsCatalogCredential cmdlet ändrar lösen ordet för autentiseringsuppgifter kopplat till en Azure Data Lake Analytics-katalog.</span><span class="sxs-lookup"><span data-stu-id="e3524-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="e3524-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3524-109">EXAMPLES</span></span>

### <span data-ttu-id="e3524-110">Exempel 1: ändra autentiseringsuppgifterna för autentiseringsuppgifter associerade med ett konto</span><span class="sxs-lookup"><span data-stu-id="e3524-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="e3524-111">Det här kommandot anger lösen ordet för autentiseringsuppgifter till det lösen ord som anges i NewPassword.</span><span class="sxs-lookup"><span data-stu-id="e3524-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="e3524-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3524-112">PARAMETERS</span></span>

### <span data-ttu-id="e3524-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="e3524-113">-Account</span></span>
<span data-ttu-id="e3524-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="e3524-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3524-115">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="e3524-115">-Credential</span></span>
<span data-ttu-id="e3524-116">Anger namn och nuvarande lösen ord för de autentiseringsuppgifter som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="e3524-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3524-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="e3524-117">-CredentialName</span></span>
<span data-ttu-id="e3524-118">Anger namnet på den autentiseringsuppgift som ska ändras</span><span class="sxs-lookup"><span data-stu-id="e3524-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="e3524-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="e3524-119">-DatabaseHost</span></span>
<span data-ttu-id="e3524-120">Anger värd namnet på den externa data källan som autentiseringsuppgiften kan ansluta till i formatet mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="e3524-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3524-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3524-121">-DatabaseName</span></span>
<span data-ttu-id="e3524-122">Anger namnet på den databas i data Lake Analytics-kontot som innehåller autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="e3524-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="e3524-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3524-123">-DefaultProfile</span></span>
<span data-ttu-id="e3524-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e3524-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3524-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="e3524-125">-NewPassword</span></span>
<span data-ttu-id="e3524-126">Anger det nya lösen ordet för autentiseringsuppgifterna</span><span class="sxs-lookup"><span data-stu-id="e3524-126">Specifies the new password for the credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3524-127">-Port</span><span class="sxs-lookup"><span data-stu-id="e3524-127">-Port</span></span>
<span data-ttu-id="e3524-128">Anger det port nummer som används för att ansluta till angiven DatabaseHost med dessa autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="e3524-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3524-129">-URI</span><span class="sxs-lookup"><span data-stu-id="e3524-129">-Uri</span></span>
<span data-ttu-id="e3524-130">Anger fullständig URI (Uniform Resource Identifier) för den externa data källan som den här autentiseringsuppgiften kan ansluta till.</span><span class="sxs-lookup"><span data-stu-id="e3524-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3524-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3524-131">-Confirm</span></span>
<span data-ttu-id="e3524-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3524-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3524-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3524-133">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3524-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3524-134">CommonParameters</span></span>
<span data-ttu-id="e3524-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3524-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3524-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3524-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3524-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3524-137">INPUTS</span></span>

### <span data-ttu-id="e3524-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e3524-138">System.String</span></span>

### <span data-ttu-id="e3524-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="e3524-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="e3524-140">System. URI</span><span class="sxs-lookup"><span data-stu-id="e3524-140">System.Uri</span></span>

### <span data-ttu-id="e3524-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e3524-141">System.Int32</span></span>

## <span data-ttu-id="e3524-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3524-142">OUTPUTS</span></span>

### <span data-ttu-id="e3524-143">Microsoft. Azure. Management. DataLake. Analytics. Models. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="e3524-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="e3524-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3524-144">NOTES</span></span>

## <span data-ttu-id="e3524-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3524-145">RELATED LINKS</span></span>
