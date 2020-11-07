---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 981baf0b0cd4d3ca70d18ab43b08bb2a16f7708f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927354"
---
# <span data-ttu-id="737ff-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="737ff-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="737ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="737ff-102">SYNOPSIS</span></span>
<span data-ttu-id="737ff-103">Aktiverar avancerad data säkerhet för en hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="737ff-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="737ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="737ff-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="737ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="737ff-105">DESCRIPTION</span></span>
<span data-ttu-id="737ff-106">Cmdleten **Enable-AzSqlInstanceAdvancedDataSecurity** aktiverar avancerad data säkerhet på en hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="737ff-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="737ff-107">Avancerad data säkerhet är ett enhetligt säkerhets paket som innehåller data klassificering, sårbarhets utvärdering och Avancerat skydd för din hanterade instans.</span><span class="sxs-lookup"><span data-stu-id="737ff-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="737ff-108">(Ett nytt lagrings konto skapas automatiskt för att spara säkerhets utvärderingar.</span><span class="sxs-lookup"><span data-stu-id="737ff-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="737ff-109">Om du har skapat ett lagrings konto för detta ändamål används det i stället.</span><span class="sxs-lookup"><span data-stu-id="737ff-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="737ff-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="737ff-110">EXAMPLES</span></span>

### <span data-ttu-id="737ff-111">Exempel 1-aktivera hanterad instans avancerad data säkerhet</span><span class="sxs-lookup"><span data-stu-id="737ff-111">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="737ff-112">Exempel 2 – aktivera hanterad instans avancerad data säkerhet från Server resurs</span><span class="sxs-lookup"><span data-stu-id="737ff-112">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="737ff-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="737ff-113">PARAMETERS</span></span>

### <span data-ttu-id="737ff-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="737ff-114">-AsJob</span></span>
<span data-ttu-id="737ff-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="737ff-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="737ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737ff-116">-DefaultProfile</span></span>
<span data-ttu-id="737ff-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="737ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="737ff-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="737ff-118">-DeploymentName</span></span>
<span data-ttu-id="737ff-119">Ange ett namn för avancerad data säkerhets distribution</span><span class="sxs-lookup"><span data-stu-id="737ff-119">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="737ff-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="737ff-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="737ff-121">Tillåt inte automatiskt sårbarhets utvärdering (det här skapar inte ett lagrings konto)</span><span class="sxs-lookup"><span data-stu-id="737ff-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="737ff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="737ff-122">-InputObject</span></span>
<span data-ttu-id="737ff-123">Det hanterade instans objekt som ska användas med den avancerade åtgärden för data säkerhets princip</span><span class="sxs-lookup"><span data-stu-id="737ff-123">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="737ff-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="737ff-124">-InstanceName</span></span>
<span data-ttu-id="737ff-125">SQL-databas hanterat instans namn.</span><span class="sxs-lookup"><span data-stu-id="737ff-125">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="737ff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737ff-126">-ResourceGroupName</span></span>
<span data-ttu-id="737ff-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="737ff-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="737ff-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="737ff-128">-Confirm</span></span>
<span data-ttu-id="737ff-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="737ff-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="737ff-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="737ff-130">-WhatIf</span></span>
<span data-ttu-id="737ff-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="737ff-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="737ff-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="737ff-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="737ff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737ff-133">CommonParameters</span></span>
<span data-ttu-id="737ff-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737ff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737ff-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="737ff-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737ff-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="737ff-136">INPUTS</span></span>

### <span data-ttu-id="737ff-137">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="737ff-137">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="737ff-138">System. String</span><span class="sxs-lookup"><span data-stu-id="737ff-138">System.String</span></span>

## <span data-ttu-id="737ff-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="737ff-139">OUTPUTS</span></span>

### <span data-ttu-id="737ff-140">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="737ff-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="737ff-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="737ff-141">NOTES</span></span>

## <span data-ttu-id="737ff-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="737ff-142">RELATED LINKS</span></span>
