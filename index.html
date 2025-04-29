import React, { useState, useEffect, useCallback } from 'react';
// Importa los iconos necesarios de lucide-react
import { Calendar as CalendarIcon, Plus, Check, Play, Pause, RotateCcw, List, LayoutGrid, Clock, Star, Tag, Target, Settings, Trash2, ChevronLeft, ChevronRight, X, ChevronDown, AlertTriangle, Bell } from 'lucide-react';

/* --- DATOS INICIALES (MOCK DATA) --- */
const initialTasks = [
  { id: 1, text: 'Preparar presentación para reunión', completed: false, priority: 'alta', dueDate: '2025-05-05', dueTime: '10:00', project: 'Trabajo', tags: ['presentación', 'importante'] },
  { id: 2, text: 'Hacer la compra semanal', completed: true, priority: 'media', dueDate: '2025-05-01', dueTime: '', project: 'Personal', tags: ['casa'] },
  { id: 3, text: 'Leer capítulo 3 del libro', completed: false, priority: 'baja', dueDate: '2025-05-10', dueTime: '18:00', project: 'Personal', tags: ['lectura'] },
  { id: 4, text: 'Llamar al fontanero', completed: false, priority: 'alta', dueDate: '2025-04-28', dueTime: '16:00', project: 'Casa', tags: ['urgente', 'casa'] }, // Vencida
  { id: 5, text: 'Planificar viaje', completed: false, priority: 'media', dueDate: '2025-05-10', dueTime: '', project: 'Personal', tags: ['viajes'] },
  { id: 6, text: 'Revisar informe mensual', completed: false, priority: 'alta', dueDate: '2025-05-20', dueTime: '09:30', project: 'Trabajo', tags: ['informe'] },
  { id: 7, text: 'Cena con amigos', completed: false, priority: 'baja', dueDate: '2025-05-05', dueTime: '20:00', project: 'Personal', tags: ['social'] },
  { id: 8, text: 'Enviar correo importante', completed: false, priority: 'alta', dueDate: '2025-04-29', dueTime: '17:00', project: 'Trabajo', tags: ['email', 'urgente'] }, // Hoy
  { id: 9, text: 'Recoger paquete', completed: false, priority: 'media', dueDate: '2025-04-29', dueTime: '19:00', project: 'Personal', tags: ['recados'] }, // Hoy
  { id: 10, text: 'Pagar factura luz', completed: false, priority: 'alta', dueDate: '2025-04-27', dueTime: '', project: 'Casa', tags: ['facturas'] }, // Vencida
];
const initialHabits = [
    { id: 1, name: 'Beber 2L de agua', completedToday: false, streak: 5 },
    { id: 2, name: 'Meditar 10 minutos', completedToday: true, streak: 12 },
    { id: 3, name: 'Hacer ejercicio', completedToday: false, streak: 3 },
];
/* --- FIN DATOS INICIALES --- */


/* --- COMPONENTES UI PERSONALIZADOS --- */
// Componente Botón con efecto pseudo-3D
const Button = ({ children, onClick, variant = 'default', size = 'default', className = '', disabled = false, ...props }) => {
  const baseStyle = 'inline-flex items-center justify-center rounded-md text-sm font-medium transition-all duration-150 ease-in-out focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-blue-500 focus-visible:ring-offset-2 ring-offset-background shadow-md active:shadow-sm active:translate-y-px';
  const variants = {
    default: 'bg-gradient-to-b from-blue-500 to-blue-700 text-white border-b-4 border-blue-800 hover:from-blue-600 hover:to-blue-800 active:border-b-2',
    destructive: 'bg-gradient-to-b from-red-500 to-red-700 text-white border-b-4 border-red-800 hover:from-red-600 hover:to-red-800 active:border-b-2',
    outline: 'border border-slate-300 bg-white text-slate-700 hover:bg-slate-50 active:bg-slate-100 border-b-4 active:border-b-2',
    secondary: 'bg-gradient-to-b from-slate-500 to-slate-700 text-white border-b-4 border-slate-800 hover:from-slate-600 hover:to-slate-800 active:border-b-2',
    ghost: 'hover:bg-slate-200 text-slate-700 active:bg-slate-300 shadow-none active:translate-y-0', // Ajustado hover/active para sidebar
    link: 'underline-offset-4 hover:underline text-blue-600 shadow-none active:translate-y-0',
    sidebarActive: 'bg-gradient-to-r from-blue-600 to-pink-500 text-white shadow-inner'
  };
  const sizes = {
    default: 'h-10 py-2 px-4',
    sm: 'h-9 px-3 rounded-md',
    lg: 'h-11 px-8 rounded-md text-base',
    icon: 'h-10 w-10',
  };
  const disabledStyle = disabled ? 'opacity-50 cursor-not-allowed pointer-events-none' : '';
  return (
    <button
      className={`${baseStyle} ${variants[variant]} ${sizes[size]} ${disabledStyle} ${className}`}
      onClick={onClick} disabled={disabled} {...props}>
      {children}
    </button>
  );
};

// Componente Input (Campo de texto)
const Input = ({ className = '', ...props }) => {
  return (
    <input
      className={`flex h-10 w-full rounded-md border border-slate-300 bg-white px-3 py-2 text-sm ring-offset-white placeholder:text-slate-400 focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-blue-500 focus-visible:ring-offset-1 disabled:cursor-not-allowed disabled:opacity-50 ${className}`}
      {...props} />
  );
};

// Componentes Card (Contenedor y partes internas)
const Card = ({ children, className = '', ...props }) => (
  <div className={`rounded-lg border border-slate-200 bg-white text-slate-900 shadow-md ${className}`} {...props}>
    {children}
  </div>
);
const CardHeader = ({ children, className = '', ...props }) => (
  <div className={`flex flex-col space-y-1.5 p-4 md:p-6 ${className}`} {...props}>{children}</div>
);
const CardTitle = ({ children, className = '', ...props }) => (
  <h3 className={`text-xl font-semibold leading-none tracking-tight text-slate-800 ${className}`} {...props}>{children}</h3>
);
const CardDescription = ({ children, className = '', ...props }) => (
  <p className={`text-sm text-slate-500 ${className}`} {...props}>{children}</p>
);
const CardContent = ({ children, className = '', ...props }) => (
  <div className={`p-4 md:p-6 pt-0 ${className}`} {...props}>{children}</div>
);
const CardFooter = ({ children, className = '', ...props }) => (
  <div className={`flex items-center p-4 md:p-6 pt-0 ${className}`} {...props}>{children}</div>
);

// Componente Checkbox
const Checkbox = ({ id, checked, onChange, className = '', ...props }) => (
  <input type="checkbox" id={id} checked={checked} onChange={onChange}
    className={`h-4 w-4 shrink-0 rounded-sm border border-slate-300 text-blue-600 focus:ring-blue-500 focus:ring-offset-white focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-blue-500 focus-visible:ring-offset-1 disabled:cursor-not-allowed disabled:opacity-50 ${className}`}
    {...props} />
);

// Componente Select (Desplegable)
const Select = ({ children, className = '', value, onChange, ...props }) => (
  <select value={value} onChange={onChange}
    className={`h-10 rounded-md border border-slate-300 bg-white px-3 py-2 text-sm ring-offset-white focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-1 ${className}`}
    {...props}>
    {children}
  </select>
);
/* --- FIN COMPONENTES UI --- */


/* --- COMPONENTES DE LA APLICACIÓN --- */

// Componente para mostrar un item de tarea individual (sin cambios)
function TaskItem({ task, onToggleComplete, onDeleteTask, isToday }) {
  const getPriorityClass = (priority) => {
    switch (priority) {
      case 'alta': return 'border-red-500';
      case 'media': return 'border-yellow-500';
      case 'baja': return 'border-green-500';
      default: return 'border-slate-300';
    }
  };
  const formatDateTime = (dateString, timeString) => {
    if (!dateString) return '';
    try {
        const dateTimeString = timeString ? `${dateString}T${timeString}` : dateString;
        const date = new Date(dateTimeString);
        if (isNaN(date.getTime())) return 'Fecha inválida';
        const dateOptions = { weekday: 'short', year: 'numeric', month: 'short', day: 'numeric' };
        const timeOptions = { hour: '2-digit', minute: '2-digit', hour12: false };
        const formattedDate = date.toLocaleDateString('es-ES', dateOptions);
        const formattedTime = timeString ? date.toLocaleTimeString('es-ES', timeOptions) : '';
        return timeString ? `${formattedDate} ${formattedTime}` : formattedDate;
    } catch (e) { console.error("Error formatting date/time:", e); return 'Fecha inválida'; }
  };
  let cardBgClass = 'bg-white hover:bg-slate-50';
  let borderClass = `border-l-4 ${getPriorityClass(task.priority)}`;
  let textColorClass = 'text-slate-800';
  if (task.completed) { cardBgClass = 'opacity-60 bg-slate-50'; textColorClass = 'line-through text-slate-500';
  } else if (task.isOverdue) { cardBgClass = 'bg-red-50 border-red-100 hover:bg-red-100'; borderClass = 'border-l-4 border-red-600'; textColorClass = 'text-red-800';
  } else if (isToday) { cardBgClass = 'bg-blue-50 border-blue-100 hover:bg-blue-100'; borderClass = `border-l-4 ${getPriorityClass(task.priority)} border-blue-500`; textColorClass = 'text-blue-800'; }
  return (
    <Card className={`mb-3 ${borderClass} ${cardBgClass} transition-colors duration-150`}>
      <CardContent className="p-3 flex items-center space-x-4">
        <Checkbox id={`task-${task.id}`} checked={task.completed} onChange={() => onToggleComplete(task.id)} aria-label={`Marcar ${task.text} como ${task.completed ? 'incompleta' : 'completa'}`} disabled={task.isOverdue && !task.completed} />
        <label htmlFor={`task-${task.id}`} className={`flex-grow ${task.completed || (task.isOverdue && !task.completed) ? '' : 'cursor-pointer'} ${textColorClass}`}>
          {task.isOverdue && !task.completed && (<AlertTriangle size={14} className="inline mr-1 text-red-600" />)}
          {isToday && !task.completed && !task.isOverdue && (<Bell size={14} className="inline mr-1 text-blue-600 animate-pulse" />)}
          <span className={`font-medium ${task.completed ? 'line-through' : ''}`}>{task.text}</span>
          <div className="text-xs text-slate-500 flex items-center flex-wrap gap-x-3 gap-y-1 mt-1">
            {(task.dueDate || task.dueTime) && (<span className="flex items-center"><CalendarIcon size={12} className="mr-1 opacity-70"/> {formatDateTime(task.dueDate, task.dueTime)}</span>)}
            {task.project && (<span className="inline-flex items-center bg-slate-100 text-slate-600 px-1.5 py-0.5 rounded text-xs"><LayoutGrid size={10} className="mr-1"/> {task.project}</span>)}
            {task.tags && task.tags.length > 0 && (<span className="flex items-center gap-1"><Tag size={12} className="opacity-70"/> {task.tags.map(tag => (<span key={tag} className="inline-block bg-blue-100 text-blue-700 px-1.5 py-0.5 rounded text-xs">{tag}</span>))}</span>)}
          </div>
        </label>
        <Button variant="ghost" size="icon" onClick={() => onDeleteTask(task.id)} aria-label={`Eliminar tarea ${task.text}`} className="text-slate-400 hover:text-red-600 hover:bg-red-100"><Trash2 size={16} /></Button>
      </CardContent>
    </Card>
  );
}

// Componente del formulario para añadir nuevas tareas (sin cambios)
function AddTaskForm({ onAddTask }) {
  const [text, setText] = useState(''); const [priority, setPriority] = useState('media'); const [dueDate, setDueDate] = useState(''); const [dueTime, setDueTime] = useState(''); const [project, setProject] = useState(''); const [tags, setTags] = useState('');
  const handleSubmit = (e) => { e.preventDefault(); if (!text.trim() || !project) { alert("Por favor, completa el texto de la tarea y selecciona un proyecto."); return; }; onAddTask({ text: text.trim(), priority, dueDate, dueTime, project, tags: tags.split(',').map(tag => tag.trim()).filter(tag => tag) }); setText(''); setPriority('media'); setDueDate(''); setDueTime(''); setProject(''); setTags(''); };
  return ( <Card className="mb-6"><CardHeader><CardTitle>Añadir Nueva Tarea</CardTitle><CardDescription>Introduce los detalles de la tarea.</CardDescription></CardHeader><CardContent><form onSubmit={handleSubmit} className="space-y-4"><Input type="text" placeholder="Describe la tarea..." value={text} onChange={(e) => setText(e.target.value)} required aria-label="Texto de la nueva tarea" /><div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4"><div><label htmlFor="priority" className="block text-sm font-medium text-slate-700 mb-1">Prioridad</label><Select id="priority" value={priority} onChange={(e) => setPriority(e.target.value)} className="w-full"><option value="alta">Alta</option><option value="media">Media</option><option value="baja">Baja</option></Select></div><div><label htmlFor="dueDate" className="block text-sm font-medium text-slate-700 mb-1">Fecha Límite</label><Input id="dueDate" type="date" value={dueDate} onChange={(e) => setDueDate(e.target.value)} className="w-full" aria-label="Fecha límite de la tarea" /></div><div><label htmlFor="dueTime" className="block text-sm font-medium text-slate-700 mb-1">Hora Límite</label><Input id="dueTime" type="time" value={dueTime} onChange={(e) => setDueTime(e.target.value)} className="w-full" aria-label="Hora límite de la tarea" /></div><div><label htmlFor="project" className="block text-sm font-medium text-slate-700 mb-1">Proyecto</label><Select id="project" value={project} onChange={(e) => setProject(e.target.value)} className="w-full" aria-label="Proyecto asociado a la tarea" required><option value="" disabled>Seleccionar...</option><option value="Personal">Personal</option><option value="Trabajo">Trabajo</option><option value="Casa">Casa</option></Select></div></div><div><label htmlFor="tags" className="block text-sm font-medium text-slate-700 mb-1">Etiquetas (separadas por coma)</label><Input id="tags" type="text" placeholder="Ej: urgente, casa" value={tags} onChange={(e) => setTags(e.target.value)} className="w-full" aria-label="Etiquetas asociadas a la tarea" /></div><Button type="submit" size="lg" className="w-full sm:w-auto"><Plus size={18} className="mr-2" /> Añadir Tarea</Button></form></CardContent></Card> );
}

// --- MODIFICADO: Componente que muestra la lista de tareas con filtro y sección Vencidas ---
function TaskList({ tasks, taskFilter, onToggleComplete, onDeleteTask }) {
  const now = new Date();
  const todayStr = now.toISOString().split('T')[0];

  // Clasifica las tareas
  const overdueTasks = [];
  const pendingTasks = [];
  const completedTasks = [];
  const todayTasks = [];

  tasks.forEach(task => {
    task.isOverdue = false;
    if (task.completed) {
      completedTasks.push(task);
    } else if (task.dueDate) {
      try {
        const deadline = new Date(task.dueDate + (task.dueTime ? `T${task.dueTime}` : 'T23:59:59'));
        if (!isNaN(deadline.getTime()) && deadline < now) {
          task.isOverdue = true;
          overdueTasks.push(task);
        } else {
          if (task.dueDate === todayStr) { todayTasks.push(task); }
          else { pendingTasks.push(task); }
        }
      } catch (e) { console.error("Error processing task deadline:", task, e); pendingTasks.push(task); }
    } else { pendingTasks.push(task); }
  });

  // Determina qué secciones mostrar basado en el filtro
  const showOverdue = taskFilter === 'all' || taskFilter === 'overdue';
  const showPending = taskFilter === 'all' || taskFilter === 'pending';
  const showCompleted = taskFilter === 'all' || taskFilter === 'completed';

  // --- CAMBIO: Solo muestra Vencidas si el filtro es 'overdue' ---
  if (taskFilter === 'overdue') {
    return (
      <div className="space-y-6">
        <div>
          <h2 className="text-xl font-semibold mb-3 text-red-400 flex items-center">
            <AlertTriangle size={20} className="mr-2"/> Tareas Vencidas ({overdueTasks.length})
          </h2>
          {overdueTasks.length > 0 ? (
            <div className="space-y-3">
              {overdueTasks.map(task => (
                <TaskItem key={task.id} task={task} onToggleComplete={onToggleComplete} onDeleteTask={onDeleteTask} isToday={false} />
              ))}
            </div>
          ) : (
            <p className="text-slate-400 italic text-center py-4">No hay tareas vencidas.</p>
          )}
        </div>
      </div>
    );
  }
   // --- FIN CAMBIO ---

  return (
    <div className="space-y-6">
      {/* Sección Tareas Vencidas (Visible solo en filtro 'all') */}
      {showOverdue && overdueTasks.length > 0 && taskFilter === 'all' && (
        <div>
          <h2 className="text-xl font-semibold mb-3 text-red-400 flex items-center">
            <AlertTriangle size={20} className="mr-2"/> Tareas Vencidas ({overdueTasks.length})
          </h2>
          <div className="space-y-3">
            {overdueTasks.map(task => (
              <TaskItem key={task.id} task={task} onToggleComplete={onToggleComplete} onDeleteTask={onDeleteTask} isToday={false} />
            ))}
          </div>
        </div>
      )}

      {/* Sección Tareas Pendientes (Visible en 'all' y 'pending') */}
      {showPending && (
        <div>
          <h2 className="text-xl font-semibold mb-3 text-slate-200">
            Tareas Pendientes ({todayTasks.length + pendingTasks.length})
          </h2>
          {todayTasks.length > 0 && (
            <div className="mb-4">
                 <h3 className="text-lg font-medium mb-2 text-blue-300 flex items-center"><Bell size={18} className="mr-2"/> Para Hoy ({todayTasks.length})</h3>
                 <div className="space-y-3">{todayTasks.map(task => (<TaskItem key={task.id} task={task} onToggleComplete={onToggleComplete} onDeleteTask={onDeleteTask} isToday={true} />))}</div>
            </div>
          )}
          {pendingTasks.length > 0 && (
             <div className="space-y-3">{pendingTasks.map(task => (<TaskItem key={task.id} task={task} onToggleComplete={onToggleComplete} onDeleteTask={onDeleteTask} isToday={false} />))}</div>
          )}
          {(todayTasks.length + pendingTasks.length) === 0 && (
            <p className="text-slate-400 italic text-center py-4">{taskFilter === 'pending' ? 'No hay tareas pendientes.' : '¡Todo al día!'}</p>
          )}
        </div>
      )}

      {/* Sección Tareas Completadas (Visible en 'all' y 'completed') */}
      {showCompleted && (
        <div>
          <h2 className="text-xl font-semibold mb-3 text-slate-200">Tareas Completadas ({completedTasks.length})</h2>
          {completedTasks.length > 0 ? (
            <div className="space-y-3">{completedTasks.map(task => (<TaskItem key={task.id} task={task} onToggleComplete={onToggleComplete} onDeleteTask={onDeleteTask} isToday={false} />))}</div>
          ) : (
             <p className="text-slate-400 italic text-center py-4">{taskFilter === 'completed' ? 'No hay tareas completadas.' : 'Aún no has completado tareas.'}</p>
          )}
        </div>
      )}
    </div>
  );
}

// Componente del temporizador Pomodoro (sin cambios)
function PomodoroTimer() { /* ...código sin cambios... */
  const WORK_DURATION = 25 * 60; const BREAK_DURATION = 5 * 60;
  const [timeLeft, setTimeLeft] = useState(WORK_DURATION); const [isActive, setIsActive] = useState(false); const [isWorkTime, setIsWorkTime] = useState(true);
  useEffect(() => { let interval = null; if (isActive && timeLeft > 0) { interval = setInterval(() => setTimeLeft(time => time - 1), 1000); } else if (isActive && timeLeft === 0) { clearInterval(interval); setIsWorkTime(!isWorkTime); setTimeLeft(isWorkTime ? BREAK_DURATION : WORK_DURATION); alert(isWorkTime ? "¡Tiempo de descanso!" : "¡De vuelta al trabajo!"); setIsActive(false); } return () => clearInterval(interval); }, [isActive, timeLeft, isWorkTime, WORK_DURATION, BREAK_DURATION]);
  const toggleTimer = () => setIsActive(!isActive); const resetTimer = () => { setIsActive(false); setIsWorkTime(true); setTimeLeft(WORK_DURATION); };
  const formatTime = (seconds) => { const minutes = Math.floor(seconds / 60); const remainingSeconds = seconds % 60; return `${minutes}:${remainingSeconds < 10 ? '0' : ''}${remainingSeconds}`; };
  return (<Card className="max-w-md mx-auto"><CardHeader className="text-center"><CardTitle>Temporizador Pomodoro</CardTitle><CardDescription>{isWorkTime ? 'Tiempo de concentración' : 'Descanso breve'}</CardDescription></CardHeader><CardContent className="text-center"><div className={`text-7xl font-bold mb-6 ${isWorkTime ? 'text-blue-600' : 'text-green-600'}`}>{formatTime(timeLeft)}</div><div className="flex justify-center space-x-4"><Button onClick={toggleTimer} variant={isActive ? "secondary" : "default"} size="lg" className="w-32">{isActive ? <><Pause size={20} className="mr-2"/> Pausar</> : <><Play size={20} className="mr-2"/> Iniciar</>}</Button><Button onClick={resetTimer} variant="outline" size="lg" className="w-32"><RotateCcw size={20} className="mr-2"/> Reiniciar</Button></div></CardContent></Card>);
 }

// Componente para rastrear hábitos (sin cambios)
function HabitTracker({ habits, onToggleHabit }) { /* ...código sin cambios... */
    return (<Card><CardHeader><CardTitle>Rastreador de Hábitos</CardTitle><CardDescription>Mantén la constancia día a día.</CardDescription></CardHeader><CardContent>{habits.length > 0 ? (<ul className="space-y-3">{habits.map(habit => (<li key={habit.id} className="flex items-center justify-between p-3 rounded-md transition-colors hover:bg-slate-50 border border-slate-200"><div className="flex items-center"><Checkbox id={`habit-${habit.id}`} checked={habit.completedToday} onChange={() => onToggleHabit(habit.id)} className="mr-3" /><label htmlFor={`habit-${habit.id}`} className="text-slate-800">{habit.name}</label></div><span className={`text-xs font-semibold px-2 py-1 rounded-full ${habit.completedToday ? 'bg-gradient-to-r from-blue-100 to-pink-100 text-blue-800' : 'bg-slate-100 text-slate-600'}`}>🔥 Racha: {habit.streak}</span></li>))}</ul>) : (<p className="text-slate-500 italic text-center py-4">No hay hábitos definidos.</p>)}</CardContent></Card>);
}

// Componente Mini Calendario Visual (sin cambios)
function MiniCalendar({ tasks, currentMonth, setCurrentMonth, onDayClick }) { /* ...código sin cambios... */
    const today = new Date(); today.setHours(0, 0, 0, 0);
    const year = currentMonth.getFullYear(); const month = currentMonth.getMonth();
    const weekdays = ['Lu', 'Ma', 'Mi', 'Ju', 'Vi', 'Sá', 'Do'];
    const firstDayOfMonth = new Date(year, month, 1); const startDayOfWeek = (firstDayOfMonth.getDay() + 6) % 7; const daysInMonth = new Date(year, month + 1, 0).getDate();
    const taskDates = React.useMemo(() => { const dates = new Set(); tasks.forEach(task => { if (task.dueDate) { try { const taskDate = new Date(task.dueDate + 'T00:00:00'); if (!isNaN(taskDate.getTime())) { dates.add(taskDate.toISOString().split('T')[0]); } } catch (e) { console.error("Error parsing task due date:", task.dueDate, e); } } }); return dates; }, [tasks]);
    const calendarDays = [];
    for (let i = 0; i < startDayOfWeek; i++) { calendarDays.push(<div key={`empty-${i}`} className="h-7 w-7"></div>); }
    for (let day = 1; day <= daysInMonth; day++) { const currentDate = new Date(year, month, day); currentDate.setHours(0,0,0,0); const dateStr = currentDate.toISOString().split('T')[0]; const isToday = currentDate.getTime() === today.getTime(); const hasTasks = taskDates.has(dateStr);
        calendarDays.push( <div key={day} onClick={hasTasks ? () => onDayClick(dateStr) : undefined} className={`h-7 w-7 flex items-center justify-center text-xs rounded-full relative ${isToday ? 'bg-blue-500 text-white font-semibold' : ''} ${hasTasks ? 'cursor-pointer hover:bg-slate-100' : 'cursor-default'} transition-colors duration-150`} title={hasTasks ? `Ver tareas para ${day}/${month+1}` : ''}> <span className={`h-6 w-6 flex items-center justify-center rounded-full ${hasTasks ? `border-2 ${isToday ? 'border-white' : 'border-pink-500'}` : ''} ${isToday && hasTasks && 'bg-blue-600'}`}> {day} </span> </div> ); }
    const goToPreviousMonth = () => setCurrentMonth(new Date(year, month - 1, 1)); const goToNextMonth = () => setCurrentMonth(new Date(year, month + 1, 1));
    return ( <Card className="mb-6 max-w-xs mx-auto"> <CardHeader className="pb-1 px-3 pt-3"> <div className="flex justify-between items-center mb-1"> <Button onClick={goToPreviousMonth} variant="ghost" size="sm" className="p-0.5 h-auto" aria-label="Mes anterior"><ChevronLeft size={16} /></Button> <CardTitle className="text-sm text-center capitalize font-semibold"> {currentMonth.toLocaleDateString('es-ES', { month: 'long', year: 'numeric' })} </CardTitle> <Button onClick={goToNextMonth} variant="ghost" size="sm" className="p-0.5 h-auto" aria-label="Mes siguiente"><ChevronRight size={16} /></Button> </div> <div className="grid grid-cols-7 gap-1 text-[10px] font-medium text-slate-500 text-center border-b pb-1 mb-1"> {weekdays.map(wd => <div key={wd}>{wd}</div>)} </div> </CardHeader> <CardContent className="pt-0 px-2 pb-2"> <div className="grid grid-cols-7 gap-0 place-items-center"> {calendarDays} </div> </CardContent> </Card> );
}

// Componente Modal para Tareas del Día (sin cambios)
function TaskModal({ isOpen, onClose, date, tasks }) { /* ...código sin cambios... */
    if (!isOpen) return null;
    const formattedDate = new Date(date + 'T00:00:00').toLocaleDateString('es-ES', { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' });
    return ( <div className="fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center z-50 p-4" onClick={onClose}> <div className="bg-white rounded-lg shadow-xl max-w-md w-full overflow-hidden" onClick={(e) => e.stopPropagation()}> <div className="flex justify-between items-center p-4 border-b border-slate-200"> <h3 className="text-lg font-semibold text-slate-800 capitalize">Tareas del {formattedDate}</h3> <Button onClick={onClose} variant="ghost" size="sm" className="p-1 h-auto" aria-label="Cerrar modal"><X size={20} /></Button> </div> <div className="p-4 max-h-80 overflow-y-auto"> {tasks.length > 0 ? ( <ul className="space-y-2"> {tasks.map(task => ( <li key={task.id} className={`text-sm p-2 rounded border-l-4 ${task.completed ? 'line-through text-slate-400 bg-slate-50 border-slate-300' : 'text-slate-700 bg-white border-blue-500'}`}> {task.text} {task.project ? `(${task.project})` : ''} </li> ))} </ul> ) : ( <p className="text-slate-500 italic text-center py-4">No hay tareas para este día.</p> )} </div> <div className="p-4 border-t border-slate-200 text-right"> <Button onClick={onClose} variant="outline" size="sm"> Cerrar </Button> </div> </div> </div> );
}

// Componente Vista de Calendario (sin cambios)
function CalendarView({ tasks }) { /* ...código sin cambios... */
    const [currentDisplayMonth, setCurrentDisplayMonth] = useState(new Date());
    const [isModalOpen, setIsModalOpen] = useState(false); const [selectedDate, setSelectedDate] = useState(null); const [tasksForModal, setTasksForModal] = useState([]);
    const handleDayClick = (dateStr) => { const tasksOnDate = tasks.filter(task => task.dueDate === dateStr); if (tasksOnDate.length > 0) { setSelectedDate(dateStr); setTasksForModal(tasksOnDate); setIsModalOpen(true); } };
    const closeModal = () => { setIsModalOpen(false); setSelectedDate(null); setTasksForModal([]); };
    const tasksForCurrentMonth = React.useMemo(() => { const year = currentDisplayMonth.getFullYear(); const month = currentDisplayMonth.getMonth(); return tasks.filter(task => { if (!task.dueDate) return false; try { const taskDate = new Date(task.dueDate + 'T00:00:00'); return !isNaN(taskDate.getTime()) && taskDate.getFullYear() === year && taskDate.getMonth() === month; } catch { return false; } }); }, [tasks, currentDisplayMonth]);
    const tasksByDate = tasksForCurrentMonth.reduce((acc, task) => { if (task.dueDate) { const date = task.dueDate; if (!acc[date]) acc[date] = []; acc[date].push(task); } return acc; }, {});
    const sortedDates = Object.keys(tasksByDate).sort((a, b) => new Date(a) - new Date(b));
    return ( <div className="space-y-6"> <MiniCalendar tasks={tasks} currentMonth={currentDisplayMonth} setCurrentMonth={setCurrentDisplayMonth} onDayClick={handleDayClick} /> <Card> <CardHeader> <CardTitle className="capitalize">Resumen de Tareas de {currentDisplayMonth.toLocaleDateString('es-ES', { month: 'long', year: 'numeric' })}</CardTitle> <CardDescription>Haz clic en un día marcado en el calendario para ver sus tareas.</CardDescription> </CardHeader> <CardContent> {sortedDates.length > 0 ? ( <div className="space-y-4"> {sortedDates.map(date => ( <div key={date}> <h3 className="font-semibold mb-2 text-blue-700 border-b pb-1 capitalize">{new Date(date + 'T00:00:00').toLocaleDateString('es-ES', { weekday: 'long', day: 'numeric' })}</h3> <ul className="list-disc pl-5 space-y-1 text-sm"> {tasksByDate[date].map(task => ( <li key={task.id} className={`${task.completed ? 'line-through text-slate-400' : 'text-slate-700'}`}> {task.text} </li> ))} </ul> </div> ))} </div> ) : ( <p className="text-slate-500 italic text-center py-4">No hay tareas programadas para este mes.</p> )} </CardContent> </Card> <TaskModal isOpen={isModalOpen} onClose={closeModal} date={selectedDate} tasks={tasksForModal} /> </div> );
}


// --- COMPONENTE PRINCIPAL DE LA APP ---
function App() {
  // Estados
  const [tasks, setTasks] = useState([]);
  const [habits, setHabits] = useState([]);
  const [karmaPoints, setKarmaPoints] = useState(0);
  const [activeView, setActiveView] = useState('tasks');
  const [isTasksMenuOpen, setIsTasksMenuOpen] = useState(true);
  // --- MODIFICADO: taskFilter ahora puede ser 'overdue' ---
  const [taskFilter, setTaskFilter] = useState('all'); // 'all', 'pending', 'completed', 'overdue'

  // Carga inicial de datos desde localStorage
  useEffect(() => {
    try {
        const savedTasks = localStorage.getItem('goplemmings_tasks');
        const loadedTasks = savedTasks ? JSON.parse(savedTasks) : initialTasks;
        setTasks(loadedTasks);
         const savedHabits = localStorage.getItem('goplemmings_habits');
        setHabits(savedHabits ? JSON.parse(savedHabits) : initialHabits);
        const savedKarma = localStorage.getItem('goplemmings_karma');
        setKarmaPoints(savedKarma ? parseInt(savedKarma, 10) : 0);
    } catch (error) { console.error("Error loading data from localStorage:", error); setTasks(initialTasks); setHabits(initialHabits); setKarmaPoints(0); }
  }, []);

  // Guarda datos en localStorage cuando cambian
  useEffect(() => { try { localStorage.setItem('goplemmings_tasks', JSON.stringify(tasks)); } catch (error) { console.error("Error saving tasks to localStorage:", error); } }, [tasks]);
  useEffect(() => { try { localStorage.setItem('goplemmings_habits', JSON.stringify(habits)); } catch (error) { console.error("Error saving habits to localStorage:", error); } }, [habits]);
  useEffect(() => { try { localStorage.setItem('goplemmings_karma', karmaPoints.toString()); } catch (error) { console.error("Error saving karma points to localStorage:", error); } }, [karmaPoints]);

  // --- FUNCIONES DE MANEJO DE DATOS ---
  const addTask = (newTaskData) => { const newTask = { id: Date.now(), ...newTaskData, completed: false, isOverdue: false }; setTasks(prevTasks => [newTask, ...prevTasks]); };
  const toggleCompleteTask = (id) => { let karmaChange = 0; setTasks(prevTasks => prevTasks.map(task => { if (task.id === id) { karmaChange = task.completed ? -5 : 5; return { ...task, completed: !task.completed }; } return task; }) ); setKarmaPoints(prev => Math.max(0, prev + karmaChange)); };
  const deleteTask = (id) => { setTasks(prevTasks => prevTasks.filter(task => task.id !== id)); };
  const toggleHabit = useCallback((id) => { let karmaChange = 0; setHabits(prevHabits => prevHabits.map(habit => { if (habit.id === id) { const completed = !habit.completedToday; let newStreak = habit.streak; if (completed) { newStreak += 1; karmaChange = 2; } else { newStreak = Math.max(0, newStreak - 1); karmaChange = -2; } return { ...habit, completedToday: completed, streak: newStreak }; } return habit; }) ); setKarmaPoints(prev => Math.max(0, prev + karmaChange)); }, []);


  // --- MODIFICADO: COMPONENTE Sidebar ---
  const Sidebar = () => {
    const handleTasksClick = () => { setActiveView('tasks'); setTaskFilter('all'); setIsTasksMenuOpen(!isTasksMenuOpen); };
    const handlePendingFilterClick = () => { setActiveView('tasks'); setTaskFilter('pending'); };
    const handleCompletedFilterClick = () => { setActiveView('tasks'); setTaskFilter('completed'); };
    // --- NUEVO: Handler para filtro Vencidas ---
    const handleOverdueFilterClick = () => { setActiveView('tasks'); setTaskFilter('overdue'); };

    return (
        <aside className="w-full md:w-72 bg-gradient-to-b from-slate-50 to-slate-100 p-5 border-r border-slate-200 flex flex-col shadow-lg">
            {/* Sección Logo y Título */}
            <div className="flex flex-col items-center mb-8 text-center">
                <img src="logo.jpg" alt="Logotipo Goplemmings Planificador" className="w-20 h-20 mb-3 rounded-full shadow-md object-cover" onError={(e) => { e.target.onerror = null; e.target.src='https://placehold.co/80x80/E2E8F0/475569?text=Logo'; }} />
                <h1 className="text-2xl font-bold bg-gradient-to-r from-blue-600 to-pink-500 bg-clip-text text-transparent" style={{ fontFamily: "'Poppins', sans-serif", fontWeight: 700, textShadow: "1px 1px 2px rgba(0,0,0,0.1)" }}>Goplemmings Planificador</h1>
            </div>

            {/* Navegación Principal */}
            <nav className="space-y-1 flex-grow">
                {/* Botón Tareas Desplegable */}
                <div>
                    <Button variant={(activeView === 'tasks' && taskFilter === 'all') ? 'sidebarActive' : 'ghost'} onClick={handleTasksClick} className="w-full justify-between text-base pr-2">
                        <span className="flex items-center"><List size={20} className="mr-3"/> Tareas</span>
                        <ChevronDown size={18} className={`transition-transform duration-200 ${isTasksMenuOpen ? 'rotate-180' : ''}`} />
                    </Button>
                    {/* Submenú Condicional */}
                    {isTasksMenuOpen && (
                        <div className="pl-8 mt-1 space-y-1">
                             <Button variant='ghost' size='sm' onClick={handlePendingFilterClick} className={`w-full justify-start text-sm ${taskFilter === 'pending' ? 'text-blue-600 font-semibold' : 'text-slate-600'}`}>Tareas Pendientes</Button>
                             <Button variant='ghost' size='sm' onClick={handleCompletedFilterClick} className={`w-full justify-start text-sm ${taskFilter === 'completed' ? 'text-blue-600 font-semibold' : 'text-slate-600'}`}>Tareas Completadas</Button>
                             {/* --- NUEVO: Botón Tareas Vencidas --- */}
                             <Button variant='ghost' size='sm' onClick={handleOverdueFilterClick} className={`w-full justify-start text-sm ${taskFilter === 'overdue' ? 'text-red-600 font-semibold' : 'text-slate-600'}`}>Tareas Vencidas</Button>
                        </div>
                    )}
                </div>
                {/* Otros botones */}
                <Button variant={activeView === 'calendar' ? 'sidebarActive' : 'ghost'} onClick={() => setActiveView('calendar')} className="w-full justify-start text-base"><CalendarIcon size={20} className="mr-3"/> Calendario</Button>
                <Button variant={activeView === 'pomodoro' ? 'sidebarActive' : 'ghost'} onClick={() => setActiveView('pomodoro')} className="w-full justify-start text-base"><Clock size={20} className="mr-3"/> Pomodoro</Button>
                <Button variant={activeView === 'habits' ? 'sidebarActive' : 'ghost'} onClick={() => setActiveView('habits')} className="w-full justify-start text-base"><Target size={20} className="mr-3"/> Hábitos</Button>
            </nav>

            {/* Sección Inferior */}
            <div className="mt-auto pt-4 border-t border-slate-200 space-y-3">
                 <div className="flex items-center justify-center text-sm font-semibold bg-gradient-to-r from-blue-100 to-pink-100 text-blue-800 p-2.5 rounded-lg shadow-inner"><Star size={18} className="mr-2 text-yellow-500"/> Karma: {karmaPoints}</div>
                 <Button variant="ghost" className="w-full justify-start text-slate-500 hover:text-slate-700 hover:bg-slate-200 text-base" disabled><Settings size={20} className="mr-3"/> Ajustes</Button>
                 <p className="text-xs text-slate-400 text-center mt-2">Creada por Goplemmings</p>
            </div>
        </aside>
      );
  }

  // --- Función para renderizar la vista seleccionada (sin cambios) ---
  const renderView = () => {
    switch (activeView) {
      case 'tasks':
        return (
          <>
            {/* Muestra el formulario SOLO si el filtro es 'all' */}
            {taskFilter === 'all' && <AddTaskForm onAddTask={addTask} />}
            {/* Pasa el filtro actual a TaskList */}
            <TaskList
                tasks={tasks}
                taskFilter={taskFilter}
                onToggleComplete={toggleCompleteTask}
                onDeleteTask={deleteTask}
            />
          </>
        );
      case 'calendar': return <CalendarView tasks={tasks} />;
      case 'pomodoro': return <PomodoroTimer />;
      case 'habits': return <HabitTracker habits={habits} onToggleHabit={toggleHabit} />;
      default: return <p className="text-center text-slate-400 mt-10">Vista no encontrada.</p>;
    }
  };

  // Estructura principal de la aplicación
  return (
    <div className="flex flex-col md:flex-row h-screen font-sans">
      <Sidebar />
      <main className="flex-1 p-4 md:p-8 lg:p-10 overflow-y-auto bg-slate-800">
        {renderView()}
      </main>
    </div>
  );
}

// Exporta el componente principal
export default App;

/* --- NOTAS ADICIONALES ---
1.  Logo y Fuente: Recuerda configurar la ruta del logo y cargar la fuente 'Poppins'.
2.  Filtro Tareas Vencidas: Se añadió la opción "Tareas Vencidas" al submenú. Al hacer clic, la vista principal mostrará únicamente las tareas no completadas cuya fecha/hora límite ya pasó.
*/
