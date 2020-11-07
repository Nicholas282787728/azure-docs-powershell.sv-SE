---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 278c80206e1221550afc5c603c618c8219ea152f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920233"
---
# <span data-ttu-id="d81f4-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="d81f4-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="d81f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d81f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d81f4-103">Aktiverar avancerad data säkerhet för en hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="d81f4-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="d81f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d81f4-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d81f4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d81f4-105">DESCRIPTION</span></span>
<span data-ttu-id="d81f4-106">Cmdleten **Enable-AzSqlInstanceAdvancedDataSecurity** aktiverar avancerad data säkerhet på en hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="d81f4-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="d81f4-107">Avancerad data säkerhet är ett enhetligt säkerhets paket som innehåller data klassificering, sårbarhets utvärdering och Avancerat skydd för din hanterade instans.</span><span class="sxs-lookup"><span data-stu-id="d81f4-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="d81f4-108">(Ett nytt lagrings konto skapas automatiskt för att spara säkerhets utvärderingar.</span><span class="sxs-lookup"><span data-stu-id="d81f4-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="d81f4-109">Om du har skapat ett lagrings konto för detta ändamål används det i stället.</span><span class="sxs-lookup"><span data-stu-id="d81f4-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="d81f4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d81f4-110">EXAMPLES</span></span>

### <span data-ttu-id="d81f4-111">Exempel 1-aktivera hanterad instans avancerad data säkerhet</span><span class="sxs-lookup"><span data-stu-id="d81f4-111">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="d81f4-112">Exempel 2 – aktivera hanterad instans avancerad data säkerhet från Server resurs</span><span class="sxs-lookup"><span data-stu-id="d81f4-112">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="d81f4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d81f4-113">PARAMETERS</span></span>

### <span data-ttu-id="d81f4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d81f4-114">-AsJob</span></span>
<span data-ttu-id="d81f4-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d81f4-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d81f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d81f4-116">-DefaultProfile</span></span>
<span data-ttu-id="d81f4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d81f4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d81f4-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d81f4-118">-DeploymentName</span></span>
<span data-ttu-id="d81f4-119">Ange ett namn för avancerad data säkerhets distribution</span><span class="sxs-lookup"><span data-stu-id="d81f4-119">Supply a custom name for Advanced Data Security deployment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d81f4-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="d81f4-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="d81f4-121">Tillåt inte automatiskt sårbarhets utvärdering (det här skapar inte ett lagrings konto)</span><span class="sxs-lookup"><span data-stu-id="d81f4-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d81f4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d81f4-122">-InputObject</span></span>
<span data-ttu-id="d81f4-123">Det hanterade instans objekt som ska användas med den avancerade åtgärden för data säkerhets princip</span><span class="sxs-lookup"><span data-stu-id="d81f4-123">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d81f4-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d81f4-124">-InstanceName</span></span>
<span data-ttu-id="d81f4-125">SQL-databas hanterat instans namn.</span><span class="sxs-lookup"><span data-stu-id="d81f4-125">SQL Database managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d81f4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d81f4-126">-ResourceGroupName</span></span>
<span data-ttu-id="d81f4-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d81f4-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="d81f4-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d81f4-128">-Confirm</span></span>
<span data-ttu-id="d81f4-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d81f4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d81f4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d81f4-130">-WhatIf</span></span>
<span data-ttu-id="d81f4-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d81f4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d81f4-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d81f4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d81f4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d81f4-133">CommonParameters</span></span>
<span data-ttu-id="d81f4-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d81f4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d81f4-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d81f4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d81f4-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d81f4-136">INPUTS</span></span>

### <span data-ttu-id="d81f4-137">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d81f4-137">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="d81f4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d81f4-138">System.String</span></span>

## <span data-ttu-id="d81f4-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d81f4-139">OUTPUTS</span></span>

### <span data-ttu-id="d81f4-140">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d81f4-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="d81f4-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d81f4-141">NOTES</span></span>

## <span data-ttu-id="d81f4-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d81f4-142">RELATED LINKS</span></span>
