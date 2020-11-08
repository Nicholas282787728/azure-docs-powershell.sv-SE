---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263382"
---
# <span data-ttu-id="b6971-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="b6971-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="b6971-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6971-102">SYNOPSIS</span></span>
<span data-ttu-id="b6971-103">Redundans en hanterad Azure SQL-instans.</span><span class="sxs-lookup"><span data-stu-id="b6971-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="b6971-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6971-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6971-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6971-105">DESCRIPTION</span></span>
<span data-ttu-id="b6971-106">Cmdleten **Invoke-AzSqlInstanceFailover** kör en Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="b6971-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="b6971-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6971-107">EXAMPLES</span></span>

### <span data-ttu-id="b6971-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b6971-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="b6971-109">Det här kommandot kommer att redundansväxla den primära repliken för förekomsten med namnet "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="b6971-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="b6971-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b6971-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="b6971-111">Det här kommandot kommer att redundansväxla den läsbara sekundära repliken av den hanterade instansen "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="b6971-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="b6971-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6971-112">PARAMETERS</span></span>

### <span data-ttu-id="b6971-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6971-113">-AsJob</span></span>
<span data-ttu-id="b6971-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b6971-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6971-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6971-115">-DefaultProfile</span></span>
<span data-ttu-id="b6971-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6971-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6971-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b6971-117">-Force</span></span>
<span data-ttu-id="b6971-118">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="b6971-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b6971-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b6971-119">-Name</span></span>
<span data-ttu-id="b6971-120">Namnet på den Azure SQL-instans som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b6971-120">The name of the Azure SQL instance to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6971-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6971-121">-PassThru</span></span>
<span data-ttu-id="b6971-122">Returnerar true när den körs.</span><span class="sxs-lookup"><span data-stu-id="b6971-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="b6971-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b6971-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b6971-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="b6971-124">-ReadableSecondary</span></span>
<span data-ttu-id="b6971-125">Redundansväxla den läsbara sekundära repliken i stället för den primära standard repliken</span><span class="sxs-lookup"><span data-stu-id="b6971-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="b6971-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6971-126">-ResourceGroupName</span></span>
<span data-ttu-id="b6971-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b6971-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="b6971-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6971-128">-Confirm</span></span>
<span data-ttu-id="b6971-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6971-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6971-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6971-130">-WhatIf</span></span>
<span data-ttu-id="b6971-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6971-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6971-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6971-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6971-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6971-133">CommonParameters</span></span>
<span data-ttu-id="b6971-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6971-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6971-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6971-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6971-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6971-136">INPUTS</span></span>

### <span data-ttu-id="b6971-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b6971-137">System.String</span></span>

## <span data-ttu-id="b6971-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6971-138">OUTPUTS</span></span>

## <span data-ttu-id="b6971-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6971-139">NOTES</span></span>

## <span data-ttu-id="b6971-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6971-140">RELATED LINKS</span></span>
