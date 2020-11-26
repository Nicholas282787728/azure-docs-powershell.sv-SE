---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 39b23c1b39121f143791667ade542080ba70ec95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258568"
---
# <span data-ttu-id="69925-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="69925-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="69925-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69925-102">SYNOPSIS</span></span>
<span data-ttu-id="69925-103">Inaktiverar avancerad data säkerhet för en hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="69925-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="69925-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69925-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69925-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69925-105">DESCRIPTION</span></span>
<span data-ttu-id="69925-106">Cmdleten **disable-AzSqlInstanceAdvancedDataSecurity** inaktiverar avancerad data säkerhet för en hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="69925-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="69925-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69925-107">EXAMPLES</span></span>

### <span data-ttu-id="69925-108">Exempel 1 – inaktivera den hanterade instansens avancerade data säkerhet</span><span class="sxs-lookup"><span data-stu-id="69925-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="69925-109">Exempel 2 – inaktivera avancerad data säkerhet för servrar från hanterad instans resurs</span><span class="sxs-lookup"><span data-stu-id="69925-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="69925-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69925-110">PARAMETERS</span></span>

### <span data-ttu-id="69925-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69925-111">-DefaultProfile</span></span>
<span data-ttu-id="69925-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="69925-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69925-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69925-113">-InputObject</span></span>
<span data-ttu-id="69925-114">Det hanterade instans objekt som ska användas med den avancerade åtgärden för data säkerhets princip</span><span class="sxs-lookup"><span data-stu-id="69925-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="69925-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="69925-115">-InstanceName</span></span>
<span data-ttu-id="69925-116">SQL-databas hanterat instans namn.</span><span class="sxs-lookup"><span data-stu-id="69925-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="69925-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69925-117">-ResourceGroupName</span></span>
<span data-ttu-id="69925-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="69925-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="69925-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="69925-119">-Confirm</span></span>
<span data-ttu-id="69925-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="69925-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69925-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69925-121">-WhatIf</span></span>
<span data-ttu-id="69925-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="69925-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69925-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="69925-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69925-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69925-124">CommonParameters</span></span>
<span data-ttu-id="69925-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69925-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69925-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69925-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69925-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69925-127">INPUTS</span></span>

### <span data-ttu-id="69925-128">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="69925-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="69925-129">System. String</span><span class="sxs-lookup"><span data-stu-id="69925-129">System.String</span></span>

## <span data-ttu-id="69925-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69925-130">OUTPUTS</span></span>

### <span data-ttu-id="69925-131">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="69925-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="69925-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69925-132">NOTES</span></span>

## <span data-ttu-id="69925-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69925-133">RELATED LINKS</span></span>