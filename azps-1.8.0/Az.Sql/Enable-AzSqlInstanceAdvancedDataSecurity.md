---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: faf93387f068c6ee8e83653d31b96a1f3ecdef70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746784"
---
# <span data-ttu-id="74668-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="74668-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="74668-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74668-102">SYNOPSIS</span></span>
<span data-ttu-id="74668-103">Aktiverar avancerad data säkerhet för en hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="74668-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="74668-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74668-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74668-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74668-105">DESCRIPTION</span></span>
<span data-ttu-id="74668-106">Cmdleten **Enable-AzSqlInstanceAdvancedDataSecurity** aktiverar avancerad data säkerhet på en hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="74668-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="74668-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74668-107">EXAMPLES</span></span>

### <span data-ttu-id="74668-108">Exempel 1-aktivera hanterad instans avancerad data säkerhet</span><span class="sxs-lookup"><span data-stu-id="74668-108">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="74668-109">Exempel 2 – aktivera hanterad instans avancerad data säkerhet från Server resurs</span><span class="sxs-lookup"><span data-stu-id="74668-109">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="74668-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74668-110">PARAMETERS</span></span>

### <span data-ttu-id="74668-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74668-111">-DefaultProfile</span></span>
<span data-ttu-id="74668-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74668-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74668-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74668-113">-InputObject</span></span>
<span data-ttu-id="74668-114">Det hanterade instans objekt som ska användas med den avancerade åtgärden för data säkerhets princip</span><span class="sxs-lookup"><span data-stu-id="74668-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="74668-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="74668-115">-InstanceName</span></span>
<span data-ttu-id="74668-116">SQL-databas hanterat instans namn.</span><span class="sxs-lookup"><span data-stu-id="74668-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="74668-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74668-117">-ResourceGroupName</span></span>
<span data-ttu-id="74668-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="74668-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="74668-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74668-119">-Confirm</span></span>
<span data-ttu-id="74668-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74668-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74668-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74668-121">-WhatIf</span></span>
<span data-ttu-id="74668-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74668-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74668-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74668-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74668-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74668-124">CommonParameters</span></span>
<span data-ttu-id="74668-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74668-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74668-126">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74668-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74668-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74668-127">INPUTS</span></span>

### <span data-ttu-id="74668-128">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="74668-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="74668-129">System. String</span><span class="sxs-lookup"><span data-stu-id="74668-129">System.String</span></span>

## <span data-ttu-id="74668-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74668-130">OUTPUTS</span></span>

### <span data-ttu-id="74668-131">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="74668-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="74668-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74668-132">NOTES</span></span>

## <span data-ttu-id="74668-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74668-133">RELATED LINKS</span></span>
